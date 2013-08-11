# Introduction

Enter text in [Markdown](http://daringfireball.net/projects/markdown/). Use the toolbar above, or click the **?** button for formatting help.


# Substance.Data

Data.js is a data representation framework for Javascript. It's being developed in the context of Substance, an open publishing platform. With Substance.Data you can model your domain data using a simple graph-based object model that can be serialized to JSON. It's easy to manipulate and query data on the client (browser) or on the server (Node.js) by using exactly the same API.

## Usage

In your script

	var Data = require('substance-data');

Start with a schema.

    var schema = {
      "person": {
        "type": "person",
        "name": "Person",
        "properties": {
          "name": "string",
          "origin": "location"
        }
      },
      "location": {
        "type": "location",
        "name": "Location",
        "properties": {
          "name": "string",
          "citizens": ["array", "person"]
        }
      }
    };

Create a new `Data.Graph`.

    var graph = new Data.Graph(schema);
    

Add some objects.

    graph.create({
      id: "bart",
      type: "person",
      name: "Bart Simpson"
    });

    graph.set({
      id: "springfield",
      name: "Springfield",
      type: "location",
      citizens: ["bart"]
    });

Set properties.

	graph.set(["bart", "origin"], "springfield");


Querying is easy too. With `get` you can either look up a node by id or specify a path that is used to traverse the graph.

    // Return a node
    graph.get('bart');
    // => {
      id: "bart",
      type: "person",
      name: "Bart Simpson",
      "location": "springfield"
    }
    
    // Return a property
    graph.get(["springfield", "citizens"]);
    // => ["springfield"]
    
You can even do smart querying and have the correct objects returned instead of ids.

    // Return a property
    graph.query(["springfield", "citizens"]);
    // => [{id: "springfield", type: "location", citizens: ["bart"]}]


## API

API docs are not yet ready. However to get an overview of the full API please have a look at our commented [testsuite](https://github.com/substance/data/tree/master/tests).

# Substance Document

Substance Document is an open standard for manipulating structured digital documents. It helps with the *creation* and *transformation* of digital documents. It ensures *consistency*, separates *content* from *presentation* and provides an easy to use API. It depicts the heart of the Substance platform, a set of tools for content creation and distribution.

A Substance Document can range from loosly structured content involving headings and text, such as reports or articles to more complex things that you wouldn’t consider a traditional document anymore. The format is designed to be extensible, so you can create your own flavors of documents. We put a lot of thought into the design of this module. This release of Substance.Document is a result of more than 12 months of research and development, so we are looking forward to your feedback.

<!-- 
# Play with the Console

Without too much talking, just have a look yourself. The Substance Console allows you to explore some examples and to mess around with the document manipulation protocol in a playful manner.

<iframe width="800" height="600" frameborder="0" scrolling="no" src="http://interior.substance.io/document/">
</iframe>-->


# Design goals

- A document consists of a sequence of content nodes of different types (e.g. heading, text, image)
- A document is manipulated through atomic **operations**
- The **history** is tracked, so users reconstruct previous document states at any time
- Support for incremental text updates, using a protocol similar to [Google Wave](http://www.waveprotocol.org/whitepapers/operational-transform)
- Support for text **annotations** that are not part of the content, but rather an overlay
- Support for **comments** to have dicussions that can stick on content elements or annotations.


# Getting started

This section is intended to be a step to step guide on how to use the module to programmatically create and transform digital documents of any kind.

### Start tracking a new document.

    var doc = new Substance.Document({ id: "my_doc" });

### Add a first heading to the document.

	var opA = ["create", {
        "id": "h1",
        "type": "heading",
        "content": "Heading 1"
      }
    ];

    doc.apply(opA);

### Now let's add another node, this time a text node.

This operation is pretty similar to the previous one, except this time we specify `text` as the content type.

	var opB = ["create", {
        "id": "t1",
        "type": "text",
        "content": "Text 1"
      }
    ];

    doc.apply(opB);

### Position nodes
	
    var opC = [
      "position", "content", {"nodes": ["h1", "t1"], "target": 0}
    ];
    doc.apply(opC);
    
    doc.getState();

### Update an existing node

There's a special API for incrementally updating existing nodes. This works by specifying a delta operation describing only what's changed in the text.

    var opD = [
      "update", "h1", "content", [4, "ING", -3]
    ];

    doc.apply(opD);
    doc.get('h1').content; // => "HeadING 1"

### Inspect the document state

Now after executing a bunch of operations, it is a good time to inspect the current state of the document.

    doc.toJSON();
    
This is how the JSON serialization looks like:

    {
      "id": "my_document",
      "nodes": {
        "document": {
          "title": "",
          "views": ["content"]
        },
        "h1": {
          "content": "HeadING 1",
          "id": "h1",
          "type": "heading"
        },
        "t1": {
          "content": "Hey there.",
          "id": "t1",
          "type": "text"
        },
        "content": {
          "nodes": ["h1", "t1"]
        }
      }
    }

As you can see there are two nodes registered, which can be directly accessed by their `id`. In order to reflect the order of our nodes we keep a view node `content` that has a `nodes` property reflecting the node order in the document.

### Versioning

This is where things are getting exciting. Substance.Document has first-class support for versioning through [Substance.Chronicle](http://interior.substance.io/modules/chronicle.html). So if you instantiate your document with a chronicle attached, you can do time travels.

    var versionedDoc = new Substance.Document({
      chronicle: Chronicle.create()
    });

From now on, all the applies are recorded.

    versionedDoc.apply(opA);
    versionedDoc.apply(opB);
    versionedDoc.apply(opC);

Now you can magically navigate the document's history, e.g. a simple undo.

    doc.chronicle.rewind();

You can also checkout a particular version by

    doc.chronicle.open(sha);


## Annotations

So far, we have a bare-metal digital document, containing two different types of content nodes. Now we'd also like to store additional contextual information, relevant to a particular portion of text within the document.

Unlike in other systems with Substance annotations are not part of the content itself. They're completely separated from the text. Most text editors offer the ability to emphasize portions of text using markup. E.g. in HTML it looks like this.

    <em>Emphasized term</em> in a text body.

In Substance however, we keep annotations external and remember the position of the first character, as well as an offset (how many characters are effected). An annotation emphasizing the "Hey" in "Hey there." looks like so:


### Insert annotation

Like document content, annotations are manipulated through operations.


    var op = ["annotate", "content", {
        "id": "a1",
        "type": "emphasis",
        "range": {start: [0,1], end: [0, 5]}
      }
    ];
    
    document.apply(op);

## Comments

Substance has in mind the usecase of collaborative composition of documents. Thus it allows a lively discussion during the editing process.

So if you wanted to support comments in your document model, you can can just define a new annotation type `comment` and stick it on either a content node or reference an annotation.

To learn about the full API, please consult our [test suite](https://github.com/substance/document/blob/master/tests). It should be easy to follow the examples.