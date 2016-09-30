# Open Terms and Definitions for Materials, Manufacturing, and Design
## Background
During the creation of ontologies (or even XML schemas), it's very helpful to have human-readable definitions that can be associated with classes, properties and individuals.

Unfortunately, access to definitions of technical terms without legal encumbrance is quite limited.  This repository is a step in the direction of gathering definitions with unlimited or attribution only distribution rights and making them freely available to others.

Terms, definitions, and rights statements were transcribed from a number of documents or websites.

Generally there hasn't been any attempt to harmonize or relate the terms and definitions at this time.

In one case regarding Nondestructive Inspection, the glossary contained a term, an association to a test method, and a definition.  This was captured in the model by using skos:related to link the term and NDI test method.

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
If you would like to contribute **open** terms and definitions related to materials, manufacturing and design, there are three basic approaches and each approach consists of three elements for a definition:
* a term and textual definition
* a source for the definitions (document, web, personal)
* a rights statement for the definition (e.g. unlimited distribution)

### First Approach
Simply send a spreadsheet or tab/comma delimited file to semanticmatls@gmail.com
### Second Approach
Send a vocabulary file (RDF) that adheres to the schema to semanticmatls@gmail.com.  Turtle is preferred, but other serializations are fine.
### Third Approach
Fork this repository, add and commit your vocabulary file, submit a pull request.

For the last two approaches, the sample vocabulary file entitled "tnd_template_0002.ttl" can be used as a starting point. It contains sample individuals for each of the three classes:  tnd:TermAndDefinition, tnd:DefinitionSource, and tnd:RightsStatement.

A symbolic naming convention has been adopted for the individuals (class instances) in each of the three classes.

* prefix:aaa000000 - one to three alpha characters followed by six numeric characters.  The set of individuals in each class should be assigned a unique alpha character prefix.

Example:
* tnd:ab000356 - individual in class tnd:TermAndDefinition
* tnd:cd000022 - individual in class tnd:DefinitionSource
* tnd:abe000005 - individual in class tnd:RightsStatement

If you would like to place your contributed terms and definitions in a specific subclass within tnd:TermAndDefinition, please feel free to do so.  Note, however, the class structure may change in the future.

### Alpha Prefixes Already in use
* c, ds, drs

## Future Work
The ontology schema and vocabulary (individuals) will be placed into separate files.
