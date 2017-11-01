# TEMP descriptions:

# TOBE aligned withthe classes

##typePlan - 1 - Nadere aanduiding van het type ruimtelijk instrument.
##          Domein: RuimtelijkPlanOfBesluit_SV.

##beleidsmatigVerantwoordelijkeOverheid - 1 - Overheid die verantwoordelijk is voor het ruimtelijk instrument.
##          Domein: Overheden_G.

##naamOverheid - 1 - Naam van de beleidsmatig verantwoordelijke overheid. Format in de
##          vorm: gemeente …., deelgemeente/stadsdeel ….

##overheidsCode - 1 - CBS-code van de beleidsmatig verantwoordelijke overheid. Format in de
##          vorm: 4 cijfers. Ingeval deelgemeente/stadsdeel: CBS-code gemeente.

## naam - 1 - De naam van de structuurvisie volgens de (aanhaal)titel.

## locatieNaam - 0..* - naam van de locatie.

## planstatusInfo - 1 - PlanstatusEnDatum:
##                   Een samengesteld attribuut waarbij de status van de structuurvisie en de datum waarop die is toegekend wordt opgenomen:
##                  planstatus [1]: aanduiding van de planstatus.domein: Planstatus.
##                  datum [1]: waarop de planstatus toegekend is. In format jjjj-mm-dd


## besluitnummer - 0..1 - Het nummer van het vaststellingsbesluit. Alleen toegestaan en verplicht bij de planstatus vastgesteld.
                      Met constraint zie hoofdstuk 8.

##verwijzingNaarVaststellingsbesluit - 0..1 - Verwijzing naar de tekst van het vaststellingsbesluit. Alleen toegestaan en ##verplicht bij de planstatus vastgesteld. Opgenomen wordt het identificerende gedeelte van een (hyper)link naar een bestand en of ##locatie daarin. De locatie van het bestand zelf wordt niet opgenomen.
##                      De waarde kan als een hyperlink geïmplementeerd worden.
##                      Met constraint zie hoofdstuk 8.


## verwijzingNaarIllustratieInfo - 0..* - Alleen verwijzen naar illustratie(s) op het niveau plangebied.
##                  IllustratieReferentiePG: Samengesteld attribuut bestaande uit de
##                 attributen: verwijzingNaarIllustratie [1]: naam van het bestand dat de illustratie omvat. De waarde kan als een ## hyperlink geïmplementeerd worden. typeIllustratie [1]: soort illustratie. Domein: Illustratie.
##                  Met constraint zie hoofdstuk 8.


##verwijzingNaarTekstInfo - 1..3 - Verwijzing naar tekst.
##                Afhankelijk of als norm ook de IMROPT2012 is toegepast wordt er gebruik gemaakt van objectgerichte tekst
##                of niet-objectgerichte tekst.
##                1 verwijzing naar volledige beleidsdocument(en) (verplicht) en max. 1 naar volledige bijlage(n).
##                TekstReferentiePG_SV: Samengesteld attribuut waarin
##                opgenomen: verwijzingNaarTekst [1]:
##                                      Verwijzing naar de plantekst. Opgenomen wordt het identificerende gedeelte van een (hyper)link naar een bestand en of locatie daarin. De locatie van het bestand zelf wordt niet opgenomen. De waarde kan als een hyperlink geïmplementeerd worden.
##                    typeTekst [1]: aanduiding van het type tekst waarnaar verwezen wordt.
##                Domein: TeksttypePG_SV.
##                Met constraint zie hoofdstuk 8.



#====
ondergrondInfo - 1..* - OndergrondReferentie:
                Een samengesteld attribuut bestaande uit.
                ondergrondtype [1]: naam van de ondergrond volgens domein Ondergronden.
                ondergronddatumondergronddatum [1]: datum van de gebruikte ondergrond.
                Indien geen gebruik is gemaakt van een ondergrond uit het domein Ondergronden wordt een
                eenduidige referentie naar de gebruikte ondergrond(en) gegeven.


## verwijzingNaarExternPlanInfo - 0..* - ExternPlanReferentiePG_SV:
##              Een samengesteld attribuut bestaande uit:
##               - naamExternPlan [1]: naam van het externe plan/besluit.
##               - idnExternPlan [0..1]: idn van het externe plan/besluit.
##               - rolExternPlan [1]: betekenis van het externe plan/besluit in relatie tot dit plan. (Domein: RolExternPlanPG_SV)
##                constrains: Met constraint zie hoofdstuk 8.


## verwijzingNorm - 2..3 - Opname van de Norm en de praktijkrichtlijn volgens welke het instrument gecodeerd is.
##                    Vaste waarden: IMRO2012 en PRgSV2012. Indien gebruik wordt gemaakt van objectgerichte planteksten
##                    wordt ook de norm IMROPT2012 opgenomen. In dat geval geldt het gebruik van objectgerichte planteksten
##                    bij alle attributen waar dit van toepassing kan zijn.
