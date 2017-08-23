# SemanticTeamIMRO
temporary documentation IMRO standards

## Conventions

## Process

- find all unique classes and properties

maintenance?

### DoR
examples required

### DOD

### versioning
gitflow

## Style

### used constructs
#### OWL
owl:Class
owl:ObjectProperty
owl:DatatypeProperty
owl:AnnotationProperty
owl:imports

#### rdfs:
rdfs:range
rdfs:domain
rdfs:label
rdfs:subClassOf
rdfs:subPropertyOf
rdfs:isDefinedBy

#### rdf:
rdf:type
 
#### dcterms
dcterms:subject


### Naming conventions
look at INSPIRE/KKG

concepts

model
namespace ends with # 
  classes
    CamelCase
  properties

  individuals

shacl 

nodeshapes:
  identical to represetation in the model
property shapes:
  name = target + _ + propertyname
namespace shacl  = ontology + slash


### Format

## Content

### Storage
ontology, thesauri and shacle components are stored in seperate documents.

### alignment between thesauri and model
to be discussed. (maintenance

### Modules for ontology parts

### MetaData
We want to provide meaningful metadata for vocabularies, so they can be easily used, found and int
An example of a well annotated vocabulary:

### Strictness in following original source
  
How much libery to we want to take to improve the original model?
 
example 1: typePlan could better be named typeInstrument, because it denotes the type of instrument (ruimtelijk instrument), of which 'plan' is just one type.

example 2: identifiers are complex constructs in INSPIRE and similar models, to ensure global uniqueness. In RDF, a resource identifier (URI) is globally unique by default.

example 3: For a property like 'naam' (name) a more general RDF property can be used (rdf:label). This makes the data easier to consume on the data web. 

### reuse of existing vocabularies

