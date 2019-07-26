# Structure of a parsed document

## Document

A Document is the base representation of an unstructured source object, it consists of
metadata and then a content object.

A document is used as the formal representation for a source file or binary object, and should contain
features (such as text, layout, visual elements) that can then be used in Padhana to try and
enable rich interaction with the document for re-structuring it, training or labelling etc.

    Properties:
        metadata: A dictionary of this document's metadata
        content:  content

## DocumentMetadata

Document metadata is simply a collection of metadata about a document.  It is represented as a simple
python dictionary.


## ContentNode

A simple structure for holding a content node, this is any structure which can have both a value 
and metadata, where the metadata can include spatial layout, structural information and the value is the text
content itself.  The ContentNode's structure based on how the information was parsed into the platform.

    Properties:
        children: A list of child ContentNode objects
        features: A dictionary 

    Methods:
        count:
            Returns the total number of nodes under this node