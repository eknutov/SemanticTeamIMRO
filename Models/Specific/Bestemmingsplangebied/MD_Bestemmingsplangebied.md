## Bestemmingsplangebied

We hebben de klasse bestemmingsplangebied als abstracte superklasse neergezet, en aan de hand het attribuut `typePlan`, welke als bereik de enumeratie
`RuimtelijkPlanOfBesluit_BP` kent, hebben wij de concrete klasses gedefinieerd.

*[NOTE: this is under discussion.]*

Classes:
- Bestemmingsplangebied
  - Bestemmingsplan
  - Inpassingsplan
  - Rijksbestemmingsplan
  - Uitwerkingsplan
  - Wijzigingsplan



Daarnaast zien we dat in de entiteit Bestemmingsplangebied (informatie uit) verschillende entiteiten wordt samengevoegd.

In de ontologie zijn deze entiteiten als losse klasses opgenomen:

De losse klasses zijn:
- Overheid
- Ondergrond
- Vaststellingsbesluit

Dit maakt de data linkbaarder en daarmee ook waardevoller in ee n linked data ecosysteem.

We kunnen nu bijvoorbeeld links

In feite zouden de data die deze klasses uitdrukken behandeld moeten worden als referentiedata. Idealiter zouden er bestaande referentiebronnen zijn waarnaar verwezen kan worden.

Attribuut: verwijzingNaarExternPlanInfo

Deze assosiatie naar een samengesteld attribuut is gemodelleerd als volgt:
- Een abstracte relatie `ro:externPlan`
- En de conctrete relaties: `ro:muteert`, `ro:vervangt`, `ro:tenGevolgeVan`
