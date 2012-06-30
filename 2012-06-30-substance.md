# Substance

Substance is a free and open source distributed document management system designed for collaboration and making sense of digital information in a new way.

## Modules

Substance has very modular architecture. Lower level modules such as our rich text editing programs are designed to be used in it's own right. Because everyone needs a text editor.


### Surface

Surface is intended to be an extensible low-level interface for rich text editing. It doesn't introduce any UI components, but an API for managing user-defined text annotations. For an implementation of a ritch text editor and several examples please refer to Substance Text.

### Text

A visual text editor built on Surface, providing support for text emphasis, and links. Thanks to Victor Saiz (vectorsize) for working on Surface. Substance Text is the official successor of Proper if you're wondering why this repository is now called `text`.

### Composer

The Substance Composer is a foundation for building your own editor tailored for you particular usecase. You can extend basic content types such as Text, Sections and Images with custom types such as Maps, Formulas, or pre-structured types such as an Event content type that allows you entering name, date, organizer etc.

### Library

The Substance Library is different from traditional libraries, in that there are no books stored but digital documents that are always up-to-date. Everyone with permission can read and write documents at any time. Open 24/7.


