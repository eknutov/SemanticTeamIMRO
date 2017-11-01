# Common
## skos

The skos vocabulary is located at:
[Vocabulary](common/Other/begrip.ttl)
This contains the entire vocabulary, both for the common and the specific parts.

## verwijzing

classes:

- Tekst
- teksttype enumeratie
- Illustratie
- Afbeelding
- Kaart


properties:

- verwijzing
- tekstreferentie
- illustratie
- afbeeldingsReferentie
- kaartReferentie
- illustratieverwijzing
- legendaNaam
- cartografie
- kaartNaam
- kaartNummer
- symboolCode
- externPlan
- rolExternPlan enumeratie
- verwijzingNorm
- idn


shapes:

- Teksttype_SV
- TeksttypePG_SV
- ExternPlanReferentie_SV
- ExternPlanReferentiePG_SV

## geometrie

classes:

- Geometrie

properties:

- geometrie
- idealisatie
- begrenzing

shapes:

- Idealisatie_1+2+3

## nen3610

classes:

- GeoObject
- NEN3610ID
- PlanologischGebied
- Planobject
- Plangebied

properties:

- lokaalID
- namespace
- versie
- identificatie

## overheid

classes:

- Overheid
- NationaleOverheid
- ProvincialeOverheid
- GemeentelijkeOverheid
- Deelgemeente_Stadsdeel


properties:

- beleidsmatigVerantoordelijkeOverheid
- naamOverheid
- overheidsCode

shapes:

- overheden_R


## other

classes:

- :ro
<!-- ro:RuimtelijkplanOfBesluit ekn: removed from the model -->  
- ro:Structuurvisie
- ro:Ondergrond
- ro:Instrument

properties:

- ro:locatieNaam
- ro:naam
- ro:plangebied
- ro:planobject
- ro:thema
- ro:typePlan
- ro:ondergrond
- ro:ondergrondtype
- ro:beleid
- ro:belang
- ro:rol
- ro:instrument

NamedIndividuals:

- ro:amvb
- ro:beheersverordening
- ro:bestuurlijkeAfspraken
- ro:coordinatieregeling
- ro:inpassingsplan
- ro:omgevingsvergunning
- ro:proactieveAanwijzing
- ro:reactieveAanwijzing
- ro:vooroverleg
- ro:zienswijze
- ro:verordening
- ro:voorbereidingsbesluit

shapes:

- prefixes
- RuimtelijkPlanOfBesluit_SV
- BeleidsInfo_RSV
