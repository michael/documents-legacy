## Towards open digital publishing with Substance

I'm the maintainer of [Substance](http://substance.io), an open software platform for collaborative composition and sharing of digital documents.



With this little essay, I'd like to sketch the challenges that modern publishing systems face today. I'd also like to come up with ideas how the complexity can be handled with the help of user-driven software. With Substance we're implementing some of the proposed ideas, not only to verify their feasability but to provide an Open Source publishing system. 

## Challenges of modern digital publishing

## Content Creation

First off, documents need to be written. Text needs to be annotated and structured. Images, tables and lists need to be added. Today the addition of interactive content (such as visualizations, interactive maps, etc.) becomes increasingly important and should be supported by publishing systems.

### Quality Management

In order to ensure quality and consistency of digital content, publishers need to setup a peer-review workflow. Publishing systems must provide means for reviewers to *suggest ideas*, *report errors* and offer an easy way of *communication* between reviewers and authors.

## Publishing

Once the content is complete, it's time to share it with the public. Publishing used to be a manual process consuming a substantial amount of time and expert knowledge. Digital tools are created to automatize that part. Authors should be able to put their work online themselves.

### Change Mangement / Version management

Even if the best review process were applied, all published content is prone to have errors. Over time, pieces of content need to be updated, information need to be added, and a new addition of the document needs to be published. Publishing systems 

[Eventually Consistent](http://prose.io/help/eventually-consistent.html)


- you need a smart way to deal with updates in a publishing scenario
It should be possible to publish updated versions 

### Content distribution




### Multiple target platforms

Content may be consumed on paper, online, in ebookreaders or on smart devices like (ipad iphone etc.)
- you may want to address multiple target platforms





### Peer-review processes

### Beyond markup

Markup languages such as HTML and Markdown are widely used to write and annotate digital documents. However, they are hard to handle by non-tech people.


# Substance

Substance is a content creation tool and a dead simple multi-format publishing platform. Whether you produce stories, books, documentations or scientific papers, Substance provides the tools that allow you to create, manage and share your content.


Substance is built around some core ideas:

### Content is data

Substance considers content as data, which makes them accessible to computers and allows new ways of processing them. Documents can not only be viewed, they can be queried, just like a database. Please refer to the documentation of the Substance Document module to learn how this works.

### Structured composition, using different types of content elements

Most often things work best when there are simple rules. This is why Substance cosiders documents a sequence of elements. That’s it.



are used to include style information in documents.

### Semantic editing

Instead of editing a big canvas, Substance documents are composed of content elements. While existing solutions (like Google Docs) bring traditional word-processing to the web, Substance focusses on content, by leaving the layout part to the system, not the user. Because of the absence of formatting utilities, it suggests structured content-oriented writing.

### Offline editing

You want your texts to be secure when typing.


## Architecture

The new Substance eco-system consists of an offline editing tool (The Substance Composer) and an online multi-platform publishing system (Substance.io).

### The Substance Composer

![](http://interior.substance.io/images/campaign/substance.png)

The Substance Composer is a desktop application (OSX and Linux first, Windows later), where you create and manage digital documents. While traditional text editors usually deal with visual information (emulating its representations on paper), the Substance Composer is developed around the idea that content is data. Its structured document composition allows documents to be stored and represented in multiple arbitrary ways. On top of that, with its collaborative features you can annotate, comment and revise your content with anyone. It also 


### Substance.io

![](http://interior.substance.io/images/campaign/substance.png)

Anyone can create a free account on the Substance.io server and start publishing their content online in one click straight from the Composer. You can think of it as an open document repository from where you will be able to manage your published content, add it to existing networks, find other people’s public documents or export yours in any format imaginable (print, web, tablet, mobile and more).



### How is it different from Google Docs?

Unlike Google Docs Substance focuses on structured content composition, leaving the layout part to the system not the user. Because of the absence of formatting utilities, it suggests structured, content-oriented writing. The Substance Composer is available as Open Source and can be extended by the developer community. It’s is intended to be a platform, not a product. Moreover, with Substance your data is stored locally, unless you share it with the public or a selected number of people.
