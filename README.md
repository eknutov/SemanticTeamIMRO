# SemanticTeamIMRO
temporary documentation IMRO standards

## Conventions

## Process

- find all unique **classes** and **properties**
<include short description of our process>

maintenance?

### DoR, DOD
- [DoR-DoD](DoR-DoD.md)
> Includes Definitions of Ready/Done for the model (DoR/DoD)

### Examples
- [IMRO Examples](examples)
> Model validation examples

### versioning
gitflow
- [SemanticTeamIMRO (temp location)](https://github.com/BakkerJesse/SemanticTeamIMRO)
> Temporarily using the versioning public GitHub account provides. Later to be moved to an internal Kadaster Git repository.


## Style

### used constructs
Maintained list of used constructs: [User constructs](used_constructs.md)
[comment]: # (ekn: Moved a used constructs listing to a separate file for convenience used_constructs.md otherwise this readme becomes overwhelming and unreadable)

### Naming conventions
see **INSPIRE/KKG**
* INSPIRE repo <https://github.com/inspire-eu-rdf/inspire-rdf-guidelines>
* INSPIRE docs <http://inspire-eu-rdf.github.io/inspire-rdf-guidelines/>

concepts        
[comment]: # (ekn: The purpose of listing concepts in this readme? Maybe we can have a separate file juts listing the concept names for the reference and convenience or generate that from TTL file)

**model**
- namespace ends with #
  classes
    CamelCase
  properties

  individuals

**shacl**

**nodeshapes:**
  identical to representation in the model
property shapes:
- name = target + _ + propertyname
- namespace shacl  = ontology + slash


### Format

## Content
TBD

### Storage
**ontology**, **thesauri** and **shacl** components are stored in separate documents.

### alignment between thesauri and model
TBD (maintenance phase)

### Modules for ontology parts
TBD

### MetaData
We want to provide meaningful metadata for vocabularies, so they can be easily used, found and int?
An example of a well annotated vocabulary:
[comment]: # (ekn: TODO - example of the annotated vocabulary.)

> All strings, if meaningful should be supplemented with a dutch language tag "@nl" unless they are written in English (international standard, etc. ) then "@en"
> MORE EXAMPLES TO FOLLOW HERE

### Strictness in following original source
It is allowed to deviate from the original UML model naming and structures however should? follow UML as much as possible.

```
example 1: typePlan could better be named typeInstrument, because it denotes the type of instrument (ruimtelijk instrument), of which 'plan' is just one type.
```
[comment]: # (ekn: example 2 has very little to do with the model, the point is that URIs are unique and this is a semantic model.)
```
example 2: identifiers are complex constructs in INSPIRE and similar models, to ensure global uniqueness. In RDF, a resource identifier (URI) is globally unique by default.
```
[comment]: # (ekn: example 3 name and label can be semantically different, label provides a readable resource's name, however name can denote many things (like schema:giveName) or simply be a machine readable (e.g. colour name/id: B9D3EE but the label would be "grey") it is obviously ok to use label but not because it is more "general", but rathe more descriptive for humans.)
```
example 3: For a property like 'naam' (name) a more general RDF property can be used (rdf:label). This makes the data easier to consume on the data web.
```
### reuse of existing vocabularies
Maintained list of (re)used vocabularies: [Vocabularies](vocabularies.md)

### Tools
[Atom](https://atom.io/)
- Atom packages:
  * language-rdf https://atom.io/packages/language-rdf (supports Turtle (.ttl), N-Triples (.nt) and TriG (.trig))
  * language-sparql https://atom.io/packages/language-sparql (SPARQL(.rq, .sparql) syntax highlighting)
  * languge-shexc https://atom.io/packages/language-shexc (syntax highlighting to Shape Expressions Compact Syntax)
[Brackets](http://brackets.io/)
- Brackets extensions:
  * Turtle Syntax Highlighter https://github.com/nandana/brackets-turtle-syntax-highlighter
  * SPARQL Syntax Highlighter https://github.com/nandana/brackets-sparql-syntax-highlighter
[LOD Live](http://en.lodlive.it/) - Linked data browser
