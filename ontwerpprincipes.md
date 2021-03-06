Ontwerpprincipes
----------------

Inwinning uit BGT en het bomenregister
-------------------
De referentielaag LE wordt voornamelijk gegenereerd uit gegevens in de Basisregistratie Grootschalige Topografie (BGT). De BGT bevat gegevens over wegen, terreinen, water, gebouwen, kunstwerken en andere elementen die de openbare ruimte inrichten. Het informatiemodel onder deze gegevens is het IMGeo, en bestaat uit een verplicht deel, de BGT, en een optioneel deel, IMGeo+ of plustopografie. 

RVO is één van de bronhouders van de BGT, en staat aan de lat voor het aanleveren van gegevens over percelen en landbouwgrond. Naast bronhouder is RVO ook verplicht gebruiker van de BGT voor gegevens op een kaartschaal van 1:500 tot 1:5.000. Bij hogere kaartschalen dient de Basisregistratie Topografie als basis te worden gehanteerd.

Voor de referentielaag LE worden de objecten in de BGT vertaald naar een objectcategorie Hout, Water, of Overig in de referentielaag. Bijvoorbeeld een BegroeidTerreindeel met fysiekvoorkomen ‘houtwal’ in de BGT wordt vertaal naar een object Hout met type ‘houtwal’ in de referentielaag. Voor een volledig overzicht van de vertaling van BGT naar referentielaag, zie [bijlage 1](#bijlage-1-mapping-referentielaag-le-en-bgt). Deze vertaling van BGT naar referentielaag LE is een geautomatiseerd proces op basis van business rules. Een bomenbestandvan NEO wordt gebruikt als kwaliteittoets op de bomen in de BGT en om de bomen als de houtvlakken toe te voegen aan de referentielaag. Er zouden meerdere bronnen kunnen worden gebruikt om dit voor de andere typen landschapselementen  te doen, maar hier is nog niet toe besloten. Het model bied hier wel ruimte voor met de keuzerelatie "is afgeleid van". Hier zouden nog andere referentieobjecttypen aan kunnen worden toegevoegd.

Het informatiemodel LE (IMLE) beschrijft de inhoud (gegevensdefinitie) en kwaliteit van de referentielaag landschapselementen. Het IMLE bevat aanvullende eisen op de BGT en geldt als dé standaard binnen RVO voor de referentielaag LE.


Landschapselementen
-------------------

Het IMLE onderscheid de volgende objecttypen landschapselementen. De subtypen binnen de blokjes geven een aantal voorbeelden van welke soorten landschapselementen onder andere binnen de objecttypen van de referentielaag vallen, maar dit wordt niet bijgehouden in het IMLE zelf. Wel valt het fysieke voorkomen van het BGT object te achterhalen via het BGT ID dat wordt opgeslagen. Het is bij RVO niet bekend of er vanuit de EU aanvullende eisen gelden.

<figure id="Figuur_1">
    <img src="media/Landschapselementen%20illustratie%201.png" alt="" width="100%">
    <figcaption>Overzicht landschapselementen, met voorbeelden, die landen in de referentielaag LE.</figcaption>
</figure>


Dekking
-------

Het IMLE heeft betrekking op landschapselement-objecten afkomstig uit het grondgebied van landbouwpercelen met een
omliggende strook (buffer) van 5 meter. Een landbouwperceel is een stuk grondgebied dat wordt gebruikt voor agrarische toepassingen, dat bij het Kadaster is geregistreerd op naam van een eigenaar. Een referentieperceel is alleen de beteelbare oppervlakte van dit landbouwperceel. De kadastrale oppervlakte is groter dan de beteelbare oppervlakte en bevat bijvoorbeeld soms de helft van de sloot. De landschapselementen in en binnen de buffer rond het perceel, komen terecht in de referentielaag landschapselementen. En daarnaast gaat het RVO ook handmatige insluitingen, buiten de kaders om, toestaan. Niet tot de inhoud van het IMLE behoren de (niet-agrarische) landschapselementen die buiten dit grongebied vallen. Daarnaast bestaan er ook nog uitsluitingen o.b.v. oppervlakte van het landschapselement, bijvoorbeeld Hout & Overig mag niet groter zijn dan 1.5 ha.


Modellering
-----------

Het IMLE hanteert het Metamodel voor Informatiemodellering [[MIM11]] versie 1.1 voor de
modellering van het IMLE. Het IMLE volgt hierbij de regels die horen bij een [MIM Niveau 2 conceptueel informatiemodel](https://docs.geostandaarden.nl/mim/mim/#niveau-2-conceptueel-informatiemodel). Hierbij hoort het invullen van MIM metagegevens. Voor de invulling van de keuze van het metagegeven [`Relatiemodelleringstype`](https://docs.geostandaarden.nl/mim/mim/#metagegeven-relatiemodelleringstype) gekozen voor `relatiesoort is leidend`.

Het IMLE doet een aantal suggesties voor standaarden om bij aan te sluiten, maar aangezien het een conceptueel model is, zijn deze keuzes niet definitief. Het model gaat uit van aansluiting op het het Basismodel Geo-informatie [[NEN3610]] op het gebied van semantiek. NEN 3610:2011 conformeert zich aan de [[ISO19108-2005]] en [[ISO19118-2011]] standaarden voor geo-informatie. Deze gelden daarom ook voor de IMLE. Aangezien landschapselementen direct worden ingewonnen vanuit de BGT, hanteert IMLE versie 3.1.1 van [[GML]]. Dit wijkt af van GML 3.2.2 die op de Pas-toe-of-leg-uit lijst staat van Forum Standaardisatie. Wanneer de BGT overgaat op versie 3.2.2 zal IMLE logischerwijs volgen.


