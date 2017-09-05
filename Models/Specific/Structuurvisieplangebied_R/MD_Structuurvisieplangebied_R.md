For now, all to be defined as 'common' parts of the model are included in the file and will be discussed here. At a later date, these common parts, will be migrated to a 'common' folder, including the respective discussion points here. 

*[NOTE: this is under discussion.]*


## NEN3610
The IMRO model offers an extention for a selected subset of the standard NEN3610. This subset contains the following classes:

- GeoObject
	- PlanologischGebied
		- Plangebied
		- Planobject

Each class has a `dcterms:subject` property pointing to the respective `skos:Concept`. 

As well as the following attributes:
- identificatie
- namespace
- lokaalID
- versie

`identificatie` is a composite attribute consisting out of the following properties `namespace`, `lokaalID`, `versie`. These three properties constitute the `NEN3610ID` datatype as modelled in the standard. For the Linked Data model the following approah is taken. 
- `identificatie` is a `owl:ObjectProperty` with `rdfs:range NEN3610ID`.
- NEN3610ID is an `owl:Class`.
- `namespace, lokaalID` and `versie` are `owl:DatatypeProperties` with `rdfs:range NEN3610ID`.
- In SHACL constraints are placed on `NEN3610ID`, such that exactly one `namespace` AND `lokaalID` are included and zero or one versie properties. Additionally, `sh:pattern` is used to constrain the strings objects for both `lokaalID` and `namespace`.

All resources discussed so far, are coined under a prefix, specific for nen3610, namely:
-  shacl : nen3610_str: <http://data.informatiehuisruimte.nl/def/nen3610/> 
-  rdf/owl : nen3610: <http://data.informatiehuisruimte.nl/def/nen3610#> 

The IMRO model is iteratively constructed on subclass of `plangebied` at a time. This document further narrates the modeling decisions made for the structuurvisieplangebied_R.

## Structuurvisieplangebied_R

`Structuurvisieplangebied_R` is a class, coined under the prefix:
- ro: <http://data.informatiehuisruimte.nl/def/ro#> 

## typePlan

typePlan is defined as an `owl:ObjectProperty` with a specific range. No domain is specified, but so far only instances of ro:plangebied use this property. Its range is a specific enumeration, namely `RuimtelijkPlanOfBesluit_SV`. Since this is a 'type' relation, the terms enumerated in `RuimtelijkPlanOfBesluit_SV` are defined as classes. This enumeration is a subset of another enumeration. All these are to be defined in the same hierarchy, in the model. This specific subset (`RuimtelijkPlanOfBesluit_SV`), modeled in shacl. In this case this lead to the following statement:
```
sh:in (
  ro:Structuurvisie # although only one terms is in the enumeration, for 							consistency the sh:in approach is still used.
  )
```

## Overheid

Three properties relate the structuurvisieplangebied_R with some predicate to some object related to the concept of overheid. 

- beleidsmatigVerantwoordelijkeOverheid, 
- naamOverheid, and
- overheidsCode

The latter two are used to denote and identify specifically which 'overheden' are responible for the given structuurvisieplangebied. At least one 'overheid' should be responsible for any structuurvisieplangebied. This is shown with a cardinality constraint in SHACL. A perculiarity in the IMRO standard is, that eventhough multiple 'overheden' can be responsible for a given document (indicated by the property `naamOverheid [1..*]`) only, and exactly one,'overheidsCode' is allowed. which is strange since all responsible governments can be identified by name, but only one by means of a unique code? 

In order to model this, a class 'Overheid' was included with all terms from the enumerations as subclasses. An instance of structuurvisieplangbied_R would point to an instance of the class Overheid with the predicate: `ro:beleidsmatigVerantwoordelijkeOverheid`. 
This instance then has two properties, `ro:overheidsNaam` and `ro:overheidsCode`

The cardinality of overheidsNaam is transfered to the predicate `ro: beleidsmatigVerantwoordelijkeOverheid`. ro:overheidsNaam and ro:overheidsCode both get the cardinality of exactly one. This reflects the IMRO standard in a way that multiple 'overheden' can be responsible for a given structuurvisieplangebied, but the property (and cardinality) of overheidsCode is now related to the given 'overheid', instead of the given structuurvisieplangebied.

The property 'beleidsmatigVeranwoorkdelijkeOverheid' indicates which type of government is allowed to be responsible for the given structuurvisieplangebied, and implicitly constrains the created Overheid class mentioned earlier.

In the actual data, multiple responsible governments only occur at national level. 



ro:naam not rdfs label.