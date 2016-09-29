# Open Terms and Definitions for Materials, Manufacturing, and Design
## The Basics
The vocabulary includes the definiton of a handful of classes:
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
If you would like to contribute **open** terms and definitions, you can use the sample vocbulary file entitled "tnd_template_0002.ttl" as a starting point. It contains sample individuals for each of the three classes:  tnd:TermAndDefinition, tnd:DefinitionSource, and tnd:RightsStatement.

If the terms and definitions require attribution (e.g. Creative Commons 4.0), please create individuals of type tnd:RightsStatement as needed.

If you would like to place your contributed terms and definitons in a specific subclass of tnd:TermAndDefinition, please feel free to do so.  Note, however, the class structure may change in the future.

Once you've created the file (preferably .ttl), please upload it to this directory.

## Future Work
The ontology schema will be seperated from the vocabulary.
