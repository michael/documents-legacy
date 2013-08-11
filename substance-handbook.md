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