# SemanticTeamIMRO
temporary documentation IMRO standards

## Conventions

## Process

- find all unique classes and properties
<include short description of our process>

maintenance?

### DoR
```
examples required
```

### DOD
```
examples required
```

### versioning
gitflow
```
Need to look into versioning more, for now we settle with the versioning github provides.
```

## Style

### used constructs
#### OWL
- [owl:Class](https://www.w3.org/TR/2004/REC-owl-semantics-20040210/#owl_Class)
- [owl:ObjectProperty](https://www.w3.org/TR/2004/REC-owl-semantics-20040210/#owl_ObjectProperty)
- [owl:DatatypeProperty](https://www.w3.org/TR/2004/REC-owl-semantics-20040210/#owl_DatatypeProperty)
- [owl:AnnotationProperty](https://www.w3.org/TR/2004/REC-owl-semantics-20040210/#owl_AnnotationProperty)
- [owl:imports](https://www.w3.org/TR/2004/REC-owl-semantics-20040210/#owl_imports)

#### rdfs:
- [rdfs:range](https://www.w3.org/TR/rdf-schema/#ch_range)
- [rdfs:domain](https://www.w3.org/TR/rdf-schema/#ch_domain)
- [rdfs:label](https://www.w3.org/TR/rdf-schema/#ch_label)
- [rdfs:subClassOf](https://www.w3.org/TR/rdf-schema/#ch_subclassof)
- [rdfs:subPropertyOf](https://www.w3.org/TR/rdf-schema/#ch_subpropertyof)
- [rdfs:isDefinedBy](https://www.w3.org/TR/rdf-schema/#ch_isdefinedby)

#### rdf:
- [rdf:type](https://www.w3.org/TR/2004/REC-rdf-schema-20040210/#ch_type)

#### dc/terms
- [dc:subject](http://dublincore.org/documents/2012/06/14/dcmi-terms/?v=terms#elements-subject)


### Naming conventions
look at INSPIRE/KKG
* INSPIRE repo <https://github.com/inspire-eu-rdf/inspire-rdf-guidelines>
* INSPIRE docs <http://inspire-eu-rdf.github.io/inspire-rdf-guidelines/>
```
to be refined
```
concepts

model
- namespace ends with #
  classes
    CamelCase
  properties

  individuals

shacl

nodeshapes:
  identical to represetation in the model
property shapes:
- name = target + _ + propertyname
- namespace shacl  = ontology + slash


### Format

## Content

### Storage
**ontology**, **thesauri** and **shacle** components are stored in separate documents.

### alignment between thesauri and model
to be discussed. (maintenance)

### Modules for ontology parts

### MetaData
We want to provide meaningful metadata for vocabularies, so they can be easily used, found and int
An example of a well annotated vocabulary:

All strings, if meaningful should be supplemented with a dutch languagetag "@nl"

### Strictness in following original source
allowed: deviate from names is required. Should follow UML as much as possible.

How much liberty to we want to take to improve the original model?

```
example 1: typePlan could better be named typeInstrument, because it denotes the type of instrument (ruimtelijk instrument), of which 'plan' is just one type.
```
```
example 2: identifiers are complex constructs in INSPIRE and similar models, to ensure global uniqueness. In RDF, a resource identifier (URI) is globally unique by default.
```
```
example 3: For a property like 'naam' (name) a more general RDF property can be used (rdf:label). This makes the data easier to consume on the data web.
```
### reuse of existing vocabularies

We will maintain a list of (re)used vocabularies and why, including which part of the UML model it replaced.
(and try to get away with it)


### Tools
[Atom](https://atom.io/)
- atom packages:
  * language-rdf https://atom.io/packages/language-rdf (supports Turtle (.ttl), N-Triples (.nt) and TriG (.trig))
  * language-sparql https://atom.io/packages/language-sparql (SPARQL(.rq, .sparql) syntax highlighting)
