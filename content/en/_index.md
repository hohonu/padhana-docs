---
title: Introduction
type: docs
---

# Introduction to Padhana

The Padhana framework is designed to enable you to work with PDF documents (and other types) in a
formal way.  By combining a simple document format (based on a node hierarchy) and then a
set of parsers and document analysis tools we parse and then structure/annotate document
content to enable rich interactions.

## Installation:

Source code:  https://github.com/hohonu/padhana

* For local development:
    1. Install Anaconda 3 or greater, then run:

            conda env create -f conda.yml --force
        
    2. Activate the padhana Conda environment with the command:

            conda activate padhana
        
    3. If you want to use the Tesseract Parser then you will need to install Tesseract.  See https://github.com/tesseract-ocr/tesseract/wiki for more information.

## Platform Components:

* [Documents]({{< relref "/docs/document-structure.md" >}}) are used as the formal representations for source files or binary objects, and should contain
features (such as text, layout, visual elements) that can then be used in Padhana to try and
enable rich interaction with the document for re-structuring it, labelling, training, etc.

* [Parsers]({{< relref "/docs/parsers.md" >}}) take a path to a source file and convert that file into a [Document]({{< relref "/docs/document-structure.md" >}}).

* [Connectors]({{< relref "/docs/connectors.md" >}}) take a source and provide a list of file locations (implementing the
iterator pattern).

* [Stores]({{< relref "/docs/stores.md">}}) allow you to store your parsed documents in a format that allows for quick and easy access.