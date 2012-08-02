# Roadmap

**Substance 0.5.0** will be a full rewrite, using a completely new **distributed** architecture, but with reusing a lot of code that's already there. This release should solve all the issues we identified while building our current prototype 0.4.0. We'll rewrite the editing component so we don't have to use `contenteditable` anymore. Documents will be manipulated by operations, so we can reconstruct every revision at any time.

We've got a tough roadmap to get a first working prototype out, with basic functionality.

## Stage 1 - Moving pieces

Get individual components ready.

### Substance Composer (Michael)

Implement basic document editor, supporting Section and Text nodes. Basic support and UI for user defined annotations / comments / patches. The Composer will be kept generic, so it can be integrated with different environments.

### Substance Surface (Victor)

Get ready a working version of our very own Surface.

### Substance Text (Victor)

Using the Surface, we have an interface (no UI) for custom annotations (e.g. em, strong, link or comments)

### Substance Library (Oliver)

A facility to persist and reconstruct documents. It will essentially store (append-only style) all operation that have been issued to transform a document. It should be possible to reconstruct any document state, by a given revision number.


### Substance Backend (Michael)

Deals with client sessions (Websockets, until we have our in-memory setup ready).

### Substance Frontend (Michael)

Packages the Composer, and all app-specific bits.. into the Substance Frontend. In other words, the Substance Frontend will be a reference implementation of the Substance Composer.

### Substance - The App (Michael)

The mother ship. This will be a reference implementation packaging the whole Substance stack, we'll keep this very basic, borrowing stuff from the existing Substance implementation. This app can either be installed and used locally, or in a hosted environment.

## Stage 2 - Put it all together

After completing stage two, we should have a functional package covering the functionality we have agreed on.

- Provide an API for creating and updateding documents programmatically
- Annotating documents (em, strong, links + comments)
- Patches on individual document nodes

## Stage 3 - Substance, ez-XBRL edition

Together with the Team of ez-XBRL we'll finish and polish a customized Substance build to be used for processing and annotating financial documents.

Requirements:

- export to XBRL compatible format