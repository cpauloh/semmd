# Open Terms and Definitions for Materials, Manufacturing, and Design
## Background
During the creation of ontologies (or even XML schemas), it's very helpful to have human-readable definitions that can be associated with classes, properties and individuals.

Unfortunately, access to definitions of technical terms without legal encumbrance is quite limited.  This repository is a step in the direction of gathering definitions with unlimited or attribution only distribution rights and making them freely available to others.

Terms, definitions, and rights statements were transcribed from a number of documents or websites.

Generally there hasn't been any attempt to harmonize or relate the terms and definitions at this time.

However, in one case regarding a source for Nondestructive Inspection information, the glossary contained a term, an association to a test method, and a definition.  This was captured in the model by using skos:related to link the term and NDI test method.

## Model Basics
The vocabulary includes the definition of a handful of classes:
* tnd:TermAndDefinition
  * tnd:NdiTestMethod
  * tnd:UnitOfMeasure
* tnd:DefinitonSource
* tnd:RightsStatement

![alt text][class_structure]
[class_structure]: https://github.com/cpauloh/semmd/blob/master/skos/ClassStructure.PNG "Class Structure"

and one definition of an object property:
* tnd:originalSource

A vast majority of the Terms and Definitions (T&D) are of type tnd:TermAndDefinition.  The class tnd:NdiTestMethod contains five individuals describing Nondestructive Inspection Test Methods (NDI) that are related to other terms and definitions via skos:related.

The T&D individuals within the class tnd:UnitOfMeasure will likely be deleted in the future.

## Contributing
If you would like to contribute **open** terms and definitions, you can use the sample vocabulary file entitled "tnd_template_0002.ttl" as a starting point. It contains sample individuals for each of the three classes:  tnd:TermAndDefinition, tnd:DefinitionSource, and tnd:RightsStatement.

If the terms and definitions require attribution (e.g. Creative Commons 4.0), please create individuals of type tnd:RightsStatement as needed.

If you would like to place your contributed terms and definitions in a specific subclass of tnd:TermAndDefinition, please feel free to do so.  Note, however, the class structure may change in the future.

Ideally, forking this repository, making changes, and then submitting a pull request is the preferred method for contributing.  While not required, using a turtle serialization (.ttl) is preferred.

A second method is to email your vocabulary file or even a spreadsheet containing the terms, definitions, source, and distribution rights to semanticmatls@gmail.com, and it will be added to the repository.

## Future Work
The ontology schema and vocabulary (individuals) will be placed into seperate files.
