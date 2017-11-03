The model is partitioned into several parts which each can be modelled independently (this does not mean that there is no overlap).
During the modelling of these partitions commonalities between the partitions were identified and discussed in such a way that, a super class / subclass relation is established between the common file and its partitions.
All partitions inherit classes, properties and shapes defined in the common folder and only specific, non-common, classes/properties/shapes are described in the partitions.  

## DoR (Definition of Ready)
[comment]: # (ekn: As originally stated DoR doesn't explicitly describe the resources needed to start working on a model. Model is already being worked on. Definition of Ready defines the conditions and requirements that fulfil the user story)
- a set of examples documents, descriptions, resources of various IMRO kind that cover all aspects of the model that help to verify and cover all of the user requirements (user story prerequisites)
- TODO: a test examples have to be manufactured in order to test/validate the model readiness (including the specific pats of the model)
- See [examples](examples) for more information)

## DoD (Definition of Done)
[comment]: # (ekn: need to define the DONE requirements here.)
This section describes when a model is defined as done.
For this we distinguish between the model in its entirety (such as the entire IMRO2012 standard) and parts of the model which are independently modelled and stored.

[comment]: # (ekn: There is no particular difference in DoD for the parts of the model and the entire model as a whole. Individual parts or the whole model should comply with the guidelines, have a clear separation of concerns, be verified, tested against real IMRO examples (e.g. mapping the model properties onto the GML documents partitions, tags, etc.), fulfil the user stories that are covered by the design, individual user stories as well as an epic that covers the overall model design. Removed the model (e.g. versioning has nothing to do with the modelling, it is more of a toolset and the environment where the model exists. "original: (structural similarity is less important)" what is meant by the structural similarity here?)

The partitions and the model are done when:
- the model is semantically equal to the respective partitions
- a thesauri is included with all relevant concepts in SKOS
- the model and its sub-parts include necessary metadata
- the model is verified against the examples (e.g. a subset of IMRO.gml or prepared Turtle files containing IMRO data, as well as the original UML Geonovum diagram to verify the legacy and the original design decisions)
- commonalities are identified and semantically separated from the specific parts of the model
- modelling choices are aligned throughout the partitions of the model (the model partitions are aligned with the other partitions)
- the partition is in accordance with the proposed namespace/style conventions
- TODO: to be extended
