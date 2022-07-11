Algemene principes
------------------

Coördinaat-referentiesysteem
----------------------------

Het toegepaste coördinaatsysteem voor de BGT is dat van het stelsel van de
Rijksdriehoeksmeting
([RD-stelsel](https://www.kadaster.nl/zakelijk/registraties/basisregistraties/rijksdriehoeksmeting/rijksdriehoeksstelsel)).
De coördinaatgetallen zijn daarbij op millimeternauwkeurigheid met als eenheid
meters. Het coördinaatgetal heeft maximaal drie cijfers achter de komma. Zo
nodig wordt daarvoor afgerond, zodanig dat als het vierde cijfer achter de komma
de waarde 1 t/m 4 bedraagt, het derde cijfer achter de komma niet wijzigt en als
het vierde cijfer achter de komma de waarde 5 t/m 9 bedraagt, het derde cijfer
achter de komma met één wordt verhoogd, met mogelijk ook implicaties voor de
voorliggende cijfers, waarbij dezelfde regel geldt.

De Europese richtlijn INSPIRE stelt dat binnen de Europese continentale
aardschol, waartoe ook Nederland en het Nederlandse deel van de Noordzee
behoort, geldt dat volgens het European Terrestrial Reference System 1989
(ETRS89) moet worden uitgewisseld. RD-data kan worden getransformeerd naar
ETRS89 om te voldoen aan de eisen van richtlijn INSPIRE.

Geometrie
---------

Voor de beschrijving van geometrieën geldt het [[ISO19107]] Spatial Schema. Voor
de uitwisseling wordt gebruik gemaakt van Geography Markup Language (GML) 3.1.1.
In de BGT zijn de geometrieën uit [[GML]] 3.1.1 simple features profile v1.0
toegestaan.

Zowel lijn- als vlakvormige objecten kunnen bestaan uit een boogvorm. Boogvormen
opgenomen als cirkelboog (GM_Arc) zijn niet toegestaan in het IMLE, en worden
vanuit de bronbestanden omgezet in lineaire lijnsegmenten, de zogenaamde
gestrookte boog.

Geometrietypen
--------------

De geometrietypen worden in het informatiemodel met hun [[ISO19107]] naam, zoals
GM_Surface, aangeduid. Bij objecten die een punt- of een vlakgeometrie kunnen
hebben, is een keuze element toegepast met keuze tussen punt- of vlakgeometrie.

| Geometrietype | ISO aanduiding |
|---------------|----------------|
| Vlak          | GM_Surface     |
| Lijn          | GM_Curve       |
| Punt          | GM_Point       |

Het IMLE beschrijft het geometrietype als eigenschap van een object. De
geometrietypen worden met hun [[ISO19107]]-naamgeving weergegeven. Daarbij maakt
het IMLE onderscheid in punt- of vlakgeometrie.

| Objecttype                        | Geometrietype |
|-----------------------------------|---------------|
| `Water landschapselement`         | Vlak          |
| `Hout landschapselement`          | Punt of Vlak  |
| `Boom referentieobject geometrie` | Punt          |
| `Boom referentieobject boomkruin` | Vlak          |
| `Overig landschapselement`        | Vlak          |
|                                   |               |

Topologie
---------

De vlakobjecten van het type Water, Hout, Overig op maaiveldniveau richten een
deel van het landbouwperceel in dat volgens de grondgebonden regelingen (zie het
[wettelijk kader](https://geonovum.github.io/IMLE/scope/#wettelijk-kader) in het
scope document) een subsidiabel landschapselement is. Voor objecten in het IMLE
gelden o.a. de volgende topologische relaties:

-   Elk van deze objecten topologisch gestructureerd moet zijn;

-   Objecten van hetzelfde type mogen niet overlappen.

Verder gelden de volgende topologische regels:

-   Hout mag wel overlappen met Water, maar Hout en Overig en Water mogen niet
    overlappen. (Een oever wordt geclassificeerd als Water.)

-   Een boom (Hout object met een puntgeometrie), mag niet overlappen met een
    houtvlak (Hout object met een vlakgeometrie).

Niveauaanduidingen per object
-----------------------------

Het IMLE is een tweedimensionale objectverzameling. In de BGT is het
noodzakelijk om de relatieve hoogteligging van objecten ten opzichte van elkaar
vast te leggen. Voor de referentielaag landschapselementen is het alleen
relevant om te weten welke oppervlakte van het landbouwperceel een subsidiabel
landschapselement is, want dit is voldoende om subsidie te kunnen verlenen.
Alleen bij de boom wordt misschien de hoogte vastgelegd met het attribuut
‘absoluteHoogte’.

Identificatie
-------------

IMLE is een conceptueel informatiemodel, dus de uitwerking van identificaties is
nog niet op logisch niveau. Het voorstel is om de [[NEN3610]] richtlijnen te
volgen voor identificatie. Een NEN3610ID is opgebouwd uit drie delen: een
namespace, lokaalID en versienummer. Hierbij wordt de namespace iets unieks voor
de referentielaag landschapselementen. Voor het lokaal ID wordt of het BGT ID
gebruikt voor objecten uit de bag of andere identificatie gebruikt uit het
bomenregister of een andere bron. Een landschapselement behoudt de hele
levenscyclus dezelfde identificatie.

Levensduur en historie
----------------------

Voor objecten in een informatiemodel kunnen twee tijdlijnen worden vastgelegd:
de tijdlijn in de werkelijkheid (tijdlijn geldigheid, ookwel materiële
levensduur en historie) en de tijdlijn in de registratie (tijdlijn registratie,
ookwel formele historie).

Tijdlijn registratie is geen onderdeel van een conceptueel informatiemodel en is
dan ook niet uitgewerkt in het IMLE.

Voor de `tijdlijn geldigheid` wordt de (materïele) levensduur van het
landschapselement vastgelegd. Indien mogelijk wordt deze afgeleid uit de BGT. De
levensduur van het landschapselement legt in het attribuut `begintijd` vast op
welke datum het landschapelement is ontstaan, en in het attribuut `eindtijd` op
welke datum het landschapselement is verdwenen.

Voor `objecttype Hout` wordt ook de materiële historie van het landschapselement
vastgelegd. Een `objecttype Hout` kan verschillende verschijningsvormen
(voorkomens) in de tijd hebben: een stuk terrein kan veranderen van gras- en
kruidachtigen naar bosplantsoen.

De `begintijd` van een voorkomen van een object wordt vastgelegd in het
attribuut `beginGeldigheid`, waarbij het vorige voorkomen een `eindGeldigheid`
krijgt welke gelijk is aan de «beginGeldigheid» van het volgende voorkomen.

Het IMLE volgt de regels voor object- en versiehistorie conform de BGT ([zie
paragraaf
3.9.4](https://docs.geostandaarden.nl/imgeo/catalogus/bgt/#levensduur-en-historie)).

Herkomst
--------

Bij objecten in het IMLE wordt expliciet waar de gegevens vandaan komen in de
attribuutsoort `herkomst` uit de gegevensgroep `Kwaliteit`. Wat een bron kan
zijn wordt vastgelegd in de enumeratie [Bron](#detail_class_IMLE_Bron).
