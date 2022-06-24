Datakwaliteit
=============

Het IMLE stelt eisen aan de datakwaliteit van objecten uit de referentielaag
landschapselementen, gebaseerd op de [BGT
kwaliteitseisen](https://docs.geostandaarden.nl/imgeo/catalogus/bgt/#datakwaliteit).
Dit is gedaan omdat de BGT de grootste bron is voor objecten in de
referentielaag landschapselementen. De normkwaliteit geldt generiek en per
object. De gerealiseerde kwaliteit geldt uitsluitend per plaatsbepalingspunt.

De normkwaliteit wordt beschreven volgens het [NORA Raamwerk
gegevenskwaliteit](https://www.noraonline.nl/wiki/Raamwerk_gegevenskwaliteit)
met de kwaliteitsdimensies:

-   Juistheid

    -   Positionele nauwkeurigheid

    -   Thematische nauwkeurigheid.

-   Compleetheid;

-   Validiteit;

-   Consistentie;

-   Actualiteit;

-   Precisie;

De vermelde waarden voor kwaliteit zijn minimumwaarden. Dat wil zeggen dat de
aspecten van het IMLE daar minimaal aan moeten voldoen. Betere waarden zijn
altijd toegestaan.

De tabel hieronder vermeldt de minimale waarden van de toegestane kwaliteit voor
de positionele juistheid per objecttype. In de laatste kolom staan de waarden
voor idealisatie per objecttype. Omdat IMLE bestaat uit een verzameling objecten
wordt in de tabel per object een generieke waarde voor de maximaal toegestane
afwijking vermeld tussen nabijgelegen punten met dezelfde idealisatiewaarden en
van hetzelfde object. 

| IMLE-object | Kwaliteitseisen gebaseerd op herkomst object | Actualiteit van object in maanden | Preciesie van object in cm | Idealisatie per punt van object in cm |
|-------------|---------------------------------------------------|-----------------------------------|------------------------------------------------------|---------------------------------------|
| Water       | Waterdeel                                         | 18                                | 60                                                   | ≥ 10                                  |
|             |                                                   |                                   |                                                      |                                       |
| Hout        | Begroeid terreindeel                              | 18                                | 60                                                   | ≥ 10                                  |
|             |                                                   |                                   |                                                      |                                       |
| Hout        | NEO bomenregister                                 | 4 tot 5                                | 60                                                   |                                       |
|             |                                                   |                                   |                                                      |                                       |
| Overig      | Begroeid terreindeel                              | 18                                | 60                                                   | ≥ 10                                  |
|             |                                                   |                                   |                                                      |                                       |

Tabel 1 Per objecttype generieke waarden voor actualiteit, positionele juistheid
en idealisatie

Juistheid
---------

Juistheid is de mate waarin gegevens de echte waarde goed weergeven.

### Positionele juistheid

Onder positionele juistheid verstaat men de mate waarin de opgeslagen
coördinaten overeenkomen met de waarden in de werkelijkheid of de geaccepteerde
afwijking.

De positionele juistheid van een object wordt beschreven op het niveau van het
objecttype. Hiermee wordt aan elk object binnen dat objecttype een juistheidseis
gesteld. Het IMLE hanteert voor het beschrijven van de positionele juistheid de
relatieve precisie. Een uitgebreide theoretische beschrijving hiervan staat in
het Handboek Technische Werkzaamheden van het Kadaster uit 1996 (HTW 1996). Bij
de precisiebeschrijving wordt onderscheid gemaakt tussen de relatieve precisie
van coördinaten ten gevolge van de ontstaanswijze (het meet-en
verwerkingsproces) en de idealisatie. Toepassing van het meet- en
verwerkingsproces levert de vereiste minimumwaarde op. Relatieve precisie geldt
alleen voor nabijgelegen punten.

Hieronder staan de waarden voor de minimale toegestane kwaliteit voor de
positionele juistheid van 30 en 60 cm. Het zijn afrondingen van de in het HTW
(Handboek voor de Technische Werkzaamheden van het Kadaster) 1996 vermelde
waarden voor de lengte van de halve lange as van de relatieve standaardellips
tussen twee punten in.

-   Objecten met een hoge positionele juistheid: 20 cm x √2 = 28,3 cm, afgerond:
    30 cm;

-   Objecten met een lage positionele juistheid: 40 cm x √2 = 56,6 cm, afgerond:
    60 cm.

De punten in het veld dienen te zijn ingemeten en in het bestand te zijn
verwerkt volgens de regels, zoals beschreven in de HTW van 1996, inclusief het
supplement voor detailmeten met GPS.

### Thematische nauwkeurigheid

Thematische nauwkeurigheid is beter bekend als juistheid. Het is de mate waarin
de gerelateerde gegevens in overeenstemming zijn met de werkelijke situatie in
het veld. Voor teksten en huisnummers geldt een minimumpercentage van 98%.

Compleetheid
------------

Onder Compleetheid verstaat het NORA raamwerk gegevenskwaliteit de mate waarin
IMLE-objecten die in werkelijkheid voorkomen, in het bestand aanwezig zijn. Voor
alle objecten geldt, in lijn met de BGT, een compleetheidseis van 98%.

Validiteit
----------

Validiteit is de mate waarin gegevens voldoen aan de verwachte structuur en
opslagvorm. Aan de validiteit stelt het IMLE alleen eisen in de vorm van kardinaliteiten. Kardinaliteiten vertellen hoe vaak een attribuutsoort voor mag komen binnen een objecttype. Standaard is de kardinaliteit 1, dus dan mag een attribuut 1 keer voorkomen. Een logisch informatiemodel zou ook kunnen worden gebruikt om een XSD schema te genereren waarmee de structuur en verwachte opslagvorm van gegevens kan worden gevalideerd. Aangezien IMLE een conceptueel informatiemodel is, kan het IMLE in deze vorm hier niet voor worden gebruikt.

Consistentie
------------

In de BGT wordt de relatieve hoogteligging van objecten ten opzichte van elkaar
vast gelegd. Voor IMLE is relatieveHoogte niet belangrijk, aangezien alleen de
oppervlakte op het maaiveld van landschapselementen belangrijk is. Wel wordt het Objecttype Boom referentieobject
gebruikt om de consistentie van de transformatie van BGT objecttypen naar IMLE objecttypen te verbeteren en valideren.

Actualiteit
-----------

IMLE hanteert de ISO 8601 norm voor het beschrijven van tijdsaspecten. IMLE
registreert de volgende tijden:

-   een objectBeginTijd en een objectEindTijd. Dat zijn attributen die de datum
    beschrijven waarop het object wordt geregistreerd, respectievelijk ongeldig
    wordt. Regels wanneer een object zo verandert dat er sprake is van een nieuw
    BGT object of een nieuwe versie van hetzelfde object, staan beschreven in
    paragraaf 3.10.4.

-   tijdstipRegistratie en eindRegistratie: deze attributen beschrijven het
    tijdstip waarop een versie van het object ontstaat, respectievelijk ongeldig
    wordt. Als een mutatie niet resulteert in een nieuw object, dan ontstaat een
    nieuwe versie van het object. In deze situatie ontstaat een eindRegistratie
    van de vervallen versie en een tijdstipRegistratie van de nieuwe versie van
    het object, terwijl de objectBeginTijd gelijk blijft.

-   LV-publicatiedatum: het tijdstip waarop een versie van een object in de
    Landelijke Voorziening is geregistreerd.

-   Tijdstip waarop de transformatie van BGT Objecttype naar IMLE Landschapselement werd gestart wordt vastgelegd in attribuutsoort [transformatiedatum BGT](#detail_attribute_IMLE_Kwaliteit_transformatiedatumBGT)

De notatie van de tijd is overeenkomstig de ISO-regelgeving:
jjjj-mm-ddTuu:mm:ss. De hoofdletter T wordt gebruikt om de datum- en
tijdcomponent te scheiden. Een voorbeeld: 2011-10-13T10:47:48 betekent dus 13
oktober 2011 om 10 uur 47 minuten en 48 seconden.

De kwaliteit van de tijdbeschrijving wordt beschreven met drie aspecten, te
weten tijdnauwkeurigheid, tijdconsistentie en tijdgeldigheid.

### Tijdnauwkeurigheid

Met tijdnauwkeurigheid wordt bedoeld de juistheid van de tijdswaarneming. Dit
geeft de foutmarge aan in de tijdswaarneming. IMLE legt objectlevensduur vast
met de nauwkeurigheid van de datum en formele historie met de nauwkeurigheid van
datum en tijd in uren, minuten en seconden.

### Tijdconsistentie

Met tijdconsistentie wordt de juistheid van opvolgende gebeurtenissen (events)
of tijdreeksen be­doeld. IMLE kent aan elke object een formele historie toe (zie
paragraaf 3.10.4). Formele historie bestaat uit een begin- en een eindtijd. De
eerste versie van een object ontstaat op hetzelfde moment als het object. Een
versie eindigt bij in paragraaf 3.10.3 beschreven gebeurtenissen en er ontstaat
aansluitend een nieuwe versie, behalve bij de beëindiging van een object.
Hierbij is een overlap of gat in de tijd niet toegestaan.

### Tijdgeldigheid

Tijdgeldigheid is de geldigheid van de referentielaag landschapselementen voor
de geregistreerde tijd in de registratie.

Als tijdstip (datum en tijd) voor ontstaan, wijzigen en vervallen van objecten
geldt dat hierbij de tijdzone voor Nederland van kracht is: in de winter wordt
de wintertijd aangehouden oftewel Midden-Europese Tijd (MET) en in de zomer
wordt de zomertijd aangehouden oftewel Midden-Europese Zomertijd (MEZT). Om
dubbele tijdstippen in de historie van een object te voorkomen, mag in de nacht
van zomertijd naar wintertijd tussen 02.00 u MEZT en 0.20 u MET geen mutaties
aan de referentielaag landschapselementen worden doorgevoerd.

Precisie 
---------

De mate waarin een meet- en verwerkingsproces bij herhaling dezelfde resultaten
geeft noemt men precisie. Als een hoge precisie wordt gehaald, betekent het dat
de mogelijke fout een kleine waarde heeft. Precisie is het resultaat van
inwinning en verwerking. Dat betekent dat een hoge precisie bij de inwinning
vaak ‘verslechtert’ door inpassing in een bestaand bestand. Zo zal een
terrestrische inwinning die is aangesloten op een fotogrammetrisch ingewonnen
bestand, de precisie verkrijgen die geldt voor het bestaande, fotogrammetrisch
ingewonnen be­stand. Mede om deze reden worden vaak grotere mutaties
(uitbreidingsgebieden), na controle op de betrouwbaarheid van de meting door
analyse van een eerste fase vereffening, geplaatst binnen het bestaande bestand
en niet daarop ingepast. Dit is ook bekend onder de term “dumpen”.

**Idealisatie**

Een aspect dat bij het inmeten (herkennen) van punten in het veld een
belangrijke rol speelt, is idealisatie. De idealisatieprecisie is de precisie
waarmee in het terrein een punt kan worden aangewezen, het idealiseren van een
punt. Goede idealiseerbare punten zijn bijvoorbeeld hoeken van panden, slecht
idealiseerbaar bijvoorbeeld de kant van een sloot. De idealisatieprecisie is
onafhankelijk van het gevolgde meet- en verwerkingsproces en is een absoluut
precisiekenmerk van een punt. De waarden voor idealisatie gelden daarom per punt
per objecttype en staan vermeld in de overzichttabel.

### Relatie Nauwkeurigheid – precisie en plaatsbepalingspunten

De hierboven opgenomen tabel vermeldt een generiek waarde voor de minimale
toegestane positionele juistheid (de relatieve precisie) tussen nabij gelegen
punten van één object met dezelfde idealisatie. In de praktijk zal één
IMLE-object meestal bestaan uit punten met verschillende waarden voor precisie
én idealisatie. Als men tussen deze punten of tussen nabijgelegen punten van
verschillende objecten wil toetsen, moet men eerst de maximaal toegestane
afwijking berekenen als resultaat van de gerealiseerde precisie van de
betreffende plaatsbepalingspunten én de idealisatieprecisie die geldt voor de
objecten waar deze punten deel van uit maken. Het proces daarvan is uitgebreid
beschreven in de HTW 1996.

a: puntprecisie b: idealisatieprecisie c: resulterende relatieve precisie

a: puntprecisie b: idealisatieprecisie c: resulterende relatieve precisie

*a: puntprecisie b: idealisatieprecisie c: resulterende relatieve precisie*

Als men punten over grotere afstand met elkaar wil vergelijken, moet men
rekening houden met de fouten­invloed van het gehanteerde referentiesysteem. In
Nederland is dat het stelsel van de Rijksdriehoeksmeting (RD; zie paragraaf
3.5). Toepassing van geschikte positiebepaling met behulp van satellieten (GPS,
Glonass) levert als eerste resultaat ruimtelijke coördinaten op in ETRS89. Vaak
wordt dit gezien als een ‘absoluut’ coördinaatsysteem. Om daaruit RD-coördinaten
te verkrijgen moet men in Nederland altijd een transformatie uitvoeren met de
geldige versie van RDNAPTRANS[^1].

[^1]: Zie www.rdnap.nl

Plausibiliteit
---------

Traceerbaarheid
---------
Om invulling te geven aan de kwaliteitsdimensie traseerbaarheid, wordt bij ieder Landschapsement de herkomst opgeslagen in de attribuutsoort [herkomst](#detail_attribute_IMLE_Kwaliteit_herkomst). De meeste landschapselementen worden ingewonnen uit de BGT. Hierbij is het in het kader van traceerbaarheid belangrijk dat het bgt-type of bgt-fysiekVoorkomen te traceren valt. Dit wordt gedaan door een verwijzing vast te leggen naar de specifieke BGT objecten. Hiervan kan dan het fysiek voorkomen of het type worden afgeleid. Niet ieder type landschapselement kan verwijzen naar ieder type BGT object. Een mapping hiervan is te vinden in [Bijlage 1](#bijlage-1-mapping-referentielaag-le-en-bgt).

Begrijpelijkheid
---------
