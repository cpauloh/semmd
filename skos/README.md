# Open Terms and Definitions for Materials, Manufacturing, and Design
## Background
During the creation of ontologies (or XML schemas), it's helpful to have human-understandable definitions that can be associated with classes, properties and individuals.
* When working with domain experts, it reduces the time to identify important concepts and their meaning.
* It enables software applications to present definitions to the user at the same time the machine is binding user data to elements in the ontology.
* If the definitions are published and then referred to by others within their ontologies or XML schemas, it creates another path for identifying points for alignment and/or merging.  
 * Example:  http:example.org/mmd-example/AgeHardening rdfs:seeAlso tnd:000022

Unfortunately, access to definitions of technical terms without legal encumbrance is quite limited.  This repository is a step in the direction of gathering definitions with unlimited or attribution-only licensing and making them freely available to others.

Terms, definitions, and rights statements were transcribed from a number of documents or websites.

Generally there hasn't been any attempt to harmonize or relate the terms and definitions at this time.

However, in one case regarding a source for Nondestructive Inspection (NDI) information, the glossary contained a term along with an association to a NDI test method.  This was captured in the model through the use of skos:related to link the term and NDI test method.

## Acknowledgements
[ASM International](http://www.asminternational.org/) contributed 960 high-quality definitions from their publication entitled "ASM Handbook, Volume 21: Composites."  The definitions are licensed under Creative Commons the [Attribution-ShareAlike 4.0 International](https://creativecommons.org/licenses/by-sa/4.0/) license.

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
Simply send a spreadsheet, tab delimited, or XML file to semanticmatls@gmail.com.
### Second Approach
Send a vocabulary file (RDF) adhering to the schema to semanticmatls@gmail.com.  Turtle is preferred, but other serializations are fine.
### Third Approach
Fork this repository, add and commit your vocabulary file, submit a pull request.

For the last two approaches, the sample vocabulary file entitled "tnd_template_0002.ttl" can be used as a starting point. It contains sample individuals for each of the three classes:  tnd:TermAndDefinition, tnd:DefinitionSource, and tnd:RightsStatement.

For the definition's term, the range of skos:prefLabel should be singular, lower-case, and word seperation should use spaces.  Proper nouns should be capitalized.

Examples:
* skos:prefLabel "Young's modulus"
* skos:prefLabel "tensile modulus of elasticity"

The skos:prefLabel used for tnd:DefinitionSource should use title case.

Example:
* skos:prefLabel "Technical Manual for Nondestructive Inspection Methods, Basic Theory"

The qname for each contributed term, source, and rights statement will be changed to adhere to the existing naming convention (e.g. tnd:c004678, tnd:ds053, and tnd:drs0022).  However, the original qname and its provenance will be maintained.

If you would like to place your contributed terms and definitions in a specific subclass within tnd:TermAndDefinition, please feel free to do so.  Note, however, the class structure may change in the future.


## Future Work
* The ontology schema and vocabulary (individuals) will be placed into separate files, and there will be some model refinement.
