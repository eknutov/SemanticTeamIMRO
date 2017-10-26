The model is partitioned into several parts which each can be modelled independently (this does not mean that there is no overlap).
During the modelling of these partitions commonalities between the partitions were identified and discussed in such a way that, a super class / subclass relation is established between the common file and its partitions.
All partitions inherit classes, properties and shapes defined in the common folder and only specific, non-common, classes/properties/shapes are described in the partitions.  

## DoR

This section describes all resources required in order to start working on a model.

- a set of examples documents, that cover all aspects of the model as a set.
- TODO: a test examples have to be manufactured in order to test/validate the model readiness
- See [examples](examples) for more information)


## DoD

This section describes when a model is defined as done.
For this we distinguish between the model in its entirety (such as the entire IMRO2012 standard) and parts of the model which are independently modelled and stored.


Partitions:
The partition is done when:
- when the model is semantically equal to the respective partition of the standard (structural similarity is less important),
- commonalities are identified and transfered to the common folder,
- existing vocabularies are reused if possible,
- the partition is aligned with the other partitions, i.e. modelling choices are aligned,
- the partition is in accordance with the proposed namespace/style conventions (to be investigated)


Model in its entirety:
The model is done when:
- all created partitions conform to their definition of done.
- semantics are uniformly represented
- metadata about the model is included
- versioning is included
- the model is tested on examples.
- a thesauri is included with all relevant concepts in skos.
