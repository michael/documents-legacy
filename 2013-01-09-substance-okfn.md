## Towards open digital publishing with Substance

I'm the maintainer of [Substance](http://substance.io), an open software platform for collaborative composition and sharing of digital documents. 

With this little essay, I'd like to sketch the challenges that modern publishing systems face today. I'd also like to come up with ideas how the complexity can be handled with the help of user-driven software. With Substance, our team is implementing some of the proposed ideas, not only to verify their feasability but also to release a full-featured and free-to-use publishing system as a modern alternative to existing publishing solutions.


## Challenges of modern digital publishing

### Content Creation

First off, documents need to be written. Text needs to be annotated and structured. Images, tables and lists need to be added. Today, the addition of interactive content (such as visualizations, interactive maps, etc.) becomes increasingly important and should be supported by publishing systems.

### Quality Management

In order to ensure quality and consistency of digital content, publishers need to setup a peer-review workflow. Publishing systems must provide means for reviewers to *suggest ideas*, *report errors* and offer an easy way of *communication* between reviewers and authors.

### Publishing

Once the content is complete, it's time to share it with the public. Publishing used to be a manual process consuming a substantial amount of time and expert knowledge. Digital tools are created to automatize that part. Authors should be able to put their work online themselves.

### Change Management

Even if the best review process were applied, all published content is prone to have inconsistencies and errors. Over time, pieces of content need to be updated, additional information added, and a new edition of the document has to be published to ensure [eventual consistency](http://prose.io/help/eventually-consistent.html). Therefore publishing systems must support incremental updates as well as an easy way for releasing new editions of publications.

### Content distribution

Content distribution is a complex issue today. While back in the day there was just paper, today content is also consumed electronically on different platforms: On the web, in Ebook Readers and on Smartphones. And they are all different.

There needs to be smart a mechanism that automagically turns one publication into a variety of formats (ePub, HTML, PDF) so as a publisher, you don't have to prepare versions for each and every platform supported.

## Solutions

### Separate content from presentation

Many traditional publishing systems that store Rich Markup (such as HTML) only allow publishing in that same format, which is a serious limitation when it comes to multi-platform publishing. How would you turn an HTML document into a printable version? How would you optimize it for ebook readers that use special document formats (e.g. Amazon Kindle)? By storing content (plain text) and annotations separately, users gain the ability of transforming their documents any format they need.

### Structured Composition



### Offline Editing

We've seen the drawbacks of online publishing solutions, such as Google Docs. It turns out that providing an offline editor can significantly improve the user experience during editing as well as guarantee data security. Information will stay private until you synchronize your publication with a public web-server. Authors can continue editing even if there's no internet connection.

### Support for Collaboration

Authoring a publication is an iterative process that may involve many authors.


### Operational Transformation

Instead or in addition to storing the current state of the document, it advantageous to capture a sequence of operations that have been applied by the author. Instead of describing a document.

### Extensibility

Editing requirements are fundamentally different among application domain. While book authors are comfortable with headings, text and images, scientists demand more advanced content types such as formulas, data-tables and visualizations to prove their research findings.


### Extensibility

### Beyond markup

Markup languages such as HTML and Markdown are widely used to write and annotate digital documents. However, they are hard to handle by people who are technically inexperienced.


# Substance

Substance is a content creation tool and a simple multi-format publishing platform. Whether you produce stories, books, documentations or scientific papers, Substance provides the tools that allow you to create, manage and share your content. Substance is built around some core ideas:

### Content is data

Substance considers content as data, which makes them accessible to computers and allows new ways of processing them. Documents can not only be viewed, they can be queried, just like a database. Please refer to the documentation of the [Substance.Document](http://interior.substance.io/document/) module to learn how this works.


### Structured composition, using different types of content elements

Most often things work best when there are simple rules. This is why Substance cosiders documents a sequence of elements. That’s it.



are used to include style information in documents.

### Semantic editing

Instead of editing a big canvas, Substance documents are composed of content elements. While existing solutions (like Google Docs) bring traditional word-processing to the web, Substance focusses on content, by leaving the layout part to the system, not the user. Because of the absence of formatting utilities, it suggests structured content-oriented writing.

## 


## Architecture

The new Substance eco-system consists of an offline editing tool (The Substance Composer) and an online multi-platform publishing system (Substance.io).

### The Substance Composer

![](http://interior.substance.io/images/campaign/substance.png)

The Substance Composer is a desktop application (OSX and Linux first, Windows later), where you create and manage digital documents. While traditional text editors usually deal with visual information (emulating its representations on paper), the Substance Composer is developed around the idea that content is data. Its structured document composition allows documents to be stored and represented in multiple arbitrary ways. On top of that, with its collaborative features you can annotate, comment and revise your content with anyone. It also 


### Substance.io

![](http://interior.substance.io/images/campaign/substance.png)

Anyone can create a free account on the Substance.io server and start publishing their content online in one click straight from the Composer. You can think of it as an open document repository from where you will be able to manage your published content, add it to existing networks, find other people’s public documents or export yours in any format imaginable (print, web, tablet, mobile and more).


# We need your help

Over the last two years, Substance has grown into a large project and has gained a lot of attention. People have been contacting us expressing their wish to integrate Substance in their application use-cases. Sadly, we have not yet reached a stage in which it can be used in production. We'd love to change that!

So we sat down, worked out a roadmap and launched a campaign.

http://pledgie.com/campaigns/18902

The goal of this campaign is to get Substance out of experimental state into a usable release. However, the more concrete our goals get, the more we see the need to spend dedicated time on it, in order to come to the day when we can say “It’s finally here!”.

With the help of your donation we could make it happen, which is exciting! If you like the idea proposed and want to see them in action, support us with your donation! 

For orientation: With a donation of 400EUR you can fund a full day of Substance development.