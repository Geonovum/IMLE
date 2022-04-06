Algemene principes
------------------

Coördinaat-referentiesysteem
----------------------------

Het toegepaste coördinaatsysteem voor het IMLE is dat van het stelsel van de
Rijksdriehoeksmeting (RD-stelsel). De coördinaatgetallen zijn daarbij op
millimeternauwkeurigheid met als eenheid meters. Het coördinaatgetal heeft
maximaal drie cijfers achter de komma. Zo nodig wordt daarvoor afgerond, zodanig
dat als het vierde cijfer achter de komma de waarde 1 t/m 4 bedraagt, het derde
cijfer achter de komma niet wijzigt en als het vierde cijfer achter de komma de
waarde 5 t/m 9 bedraagt, het derde cijfer achter de komma met één wordt
verhoogd, met mogelijk ook implicaties voor de voorliggende cijfers, waarbij
dezelfde regel geldt.

Het RD-stelsel voldoet aan de eisen van de Europese richtlijn INSPIRE. Deze
stelt dat binnen de Europese continentale aardschol, waartoe ook Nederland en
het Nederlandse deel van de Noordzee behoort, geldt dat coördinaten herleidbaar
moeten zijn tot het European Terrestrial Reference System 1989 (ETRS89) voor de
horizontale component.

Geometrie
---------

Voor de beschrijving van geometrieën geldt het ISO 19107 Spatial Schema. Voor de
uitwisseling wordt gebruik gemaakt van Geography Markup Language (GML) 3.1.1. In
de BGT zijn de geometrieën uit GML 3.1.1 simple features profile v1.0
toegestaan.

Zowel lijn- als vlakvormige objecten kunnen bestaan uit een boogvorm. Boogvormen
opgenomen als cirkelboog (GM_Arc) zijn niet toegestaan in het IMLE, en worden
vanuit de bronbestanden omgezet in lineare lijnsegmenten, de zogenaamde
gestrookte boog.

Geometrietypen
--------------

De geometrietypen worden in het informatiemodel met hun ISO 19107 naam, zoals
GM_Surface, aangeduid. Bij objecten die een lijn- of een vlakgeometrie kunnen
hebben, is een keuze element togepast met keuze tussen lijn of vlakgeometire.

| Geometrietype | ISO aanduiding |
|---------------|----------------|
| Vlak          | GM_Surface     |
| Lijn          | GM_Curve       |
| Punt          | GM_Point       |

Het IMLE beschrijft het geometrietype als eigenschap van een object. De
geometrietypen worden met hun ISO19107-naamgeving weergegeven. Daarbij maakt het
IMLE onderscheid in punt-, lijn- of vlakgeometrie.

| Objecttype | Classificatie | Geometrietype |
|------------|---------------|---------------|
| Water      | poel          | Vlak          |
|            | sloot         | Vlak          |
| Hout       | bomenrij      | Vlak          |
|            | bosje         | Punt          |
|            | haag, heg     | Lijun         |
|            | houtwal       | Vlak          |
|            | struweel      | Vlak          |
| Boom       |               | Punt          |
| Overig     |               | Punt          |
|            | laan          | Lijn          |
|            |               | Vlak          |

Topologie
---------

Voor objecten in het IMLE gelden de volgende topologische relaties.

De vlakobjecten van het type Water, Hout, Overig op maaiveldniveau partinioeren
de ruimte. Dat betekent dat:

-   elk van deze objecten topologisch gestructureerd moet zijn;

-   deze objecten naadloos op elkaar aan moeten sluiten, zodat er op
    maaiveldniveau geen gaten voorkomen;

-   deze objecten elkaar niet mogen overlappen.

Verder gelden de volgende topologische relaties:

-   Boom ligt niet in Water.

-   Inrichtend object Hout ligt niet water.

-   …

Niveauaanduidingen per object
-----------------------------

*Het IMLE is een tweedimensionale objectverzameling. Daarom is het noodzakelijk
om de rel­atieve hoogteligging van objecten ten opzichte van elkaar vast te
leggen. Hiervoor wordt gebruik gemaakt van niveaus die aangeven of een object
zich op maaiveldniveau (niveau 0) bevindt of op een onder- of bovenliggend
niveau. Het niveau wordt vastgelegd met het attribuut ‘relatieveHoogteligging’.
Dit kan elk willekeurig geheel getal (integer) aannemen. Het niveaugetal geeft
geen informatie over de absolute hoogte van een object.*

Identificatie
-------------

Elk object in het IMLE krijgt een unieke aanduiding (identificatie).

De identificatie is als volgt opgemaakt / wordt overgenomen uit de BGT?

Een landschapselement behoudt de hele levenscyclus zijn identificatie.

Levensduur en historie
----------------------

Voor objecten in een informatiemodel kunnen twee tijdlijnen worden vastgelegd:
de tijdlijn in de werkelijkheid (tijdlijn geldigheid, ookwel materiële
levensduur en historie) en de tijdlijn in de registratie (tijdlijn registratie,
ookwel formele historie).

Tijdlijn registratie is geen onderdeel van een conceptueel informatiemodel en is
dan ook niet uigewerkt in het IMLE.

Voor de tijdlijn geldigheid wordt de (materïele) levensduur van het
landschapselement vastgelegd. De levensduur van het landschapselement legt in
het attribuut begintijd vast op welke datum het landschapelement is ontstaan, en
in het attribuut eindtijd op welke datum het landschapselement is verdwenen.

Voor objecttype Hout wordt ook de materiële historie van het landschapselement
vastgelegd. Een objecttype Hout kan verschillende verschijningsvormen
(voorkomens) in de tijd hebben: een stuk terrein kan veranderen van gras- en
kruidachtigen naar bosplantsoen.

De begintijd van een voorkomen van een object wordt vastgelegd in het attribuut
«beginGeldigheid», waarbij het vorige voorkomen een «eindGeldigheid» krijgt
welke gelijk is aan de «beginGeldigheid» van het volgende voorkomen.

Het IMLE volgt de regels voor object- en versiehistorie conform de BGT (zie
paragraag 3.9.4).

NOTE:

Ter overweging: Boom en Water alleen materiële levensduur, en bij hout ook
materiële historie.

NOTE:

Moeten objecten nog statussen krijgen? Namelijk: houtwal in aanleg etc?

 Herkomst
---------

Bij objecten in het IMLE wordt expliciet waar de gegevens vandaan komen (bron).
Een bron kan zijn de BGT, BRT etc.
