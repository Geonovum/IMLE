Ontwerpprincipes
----------------

Inwinning uit BGT en het bomenregister
-------------------
De referentielaag LE wordt voornamelijk gegenereerd uit gegevens in de Basisregistratie Grootschalige Topografie (BGT). De BGT bevat gegevens over wegen, terreinen, water, gebouwen, kunstwerken en andere elementen die de openbare ruimte inrichten. Het informatiemodel onder deze gegevens is het IMGeo, en bestaat uit een verplicht deel, de BGT, en een optioneel deel, IMGeo+ of plustopografie. 

RVO is één van de bronhouders van de BGT, en staat aan de lat voor het aanleveren van gegevens over percelen en landbouwgrond. Naast bronhouder is RVO ook verplicht gebruiker van de BGT voor gegevens op een kaartschaal van 1:500 tot 1:5.000. Bij hogere kaartschalen dient de Basisregistratie Topografie als basis te worden gehanteerd.

Voor de referentielaag LE worden de objecten in de BGT vertaald naar een objectcategorie Hout, Water, of Overig in de referentielaag. Bijvoorbeeld een BegroeidTerreindeel met fysiekvoorkomen ‘houtwal’ in de BGT wordt vertaal naar een object Hout met type ‘houtwal’ in de referentielaag. Voor een volledig overzicht van de vertaling van BGT naar referentielaag, zie [bijlage 1](#bijlage-1-mapping-referentielaag-le-en-bgt). Deze vertaling van BGT naar referentielaag LE is een geautomatiseerd proces op basis van business rules. Het neo bomenregister wordt gebruikt  

Het informatiemodel LE (IMLE) beschrijft de inhoud (gegevensdefinitie) en kwaliteit van de referentielaag landschapselementen. Het IMLE bevat aanvullende eisen op de BGT en geldt als dé standaard binnen RVO voor de referentielaag LE.


Landschapselementen
-------------------

Het IMLE onderscheid de volgende objecttypen landschapselementen. De subtypen binnen de blokjes geven aan welke soorten landschapselementen onder andere binnen het objecttype vallen, maar dit wordt niet bijgehouden in het IMLE zelf. Wel valt het fysieke voorkomen van het BGT object te achterhalen via het BGT ID dat wordt opgeslagen.

<figure id="Figuur_1">
    <img src="media/93668ed4dcd7750698f8bc63ab8de72d.png" alt="" width="100%">
    <figcaption>Overzicht landschapselementen met voorbeelden van subtypereningen die landen in de referentielaag LE.</figcaption>
</figure>


Dekking
-------

Het IMLE heeft betrekking op landschapselement-objecten afkomstig uit het grondgebied van landbouwpercelen met een
omliggende strook (buffer) van 5 meter. Een landbouwperceel is een stuk grondgebied dat wordt gebruikt voor agrarische toepassingen, dat bij het Kadster is geregistreerd op naam van een eigenaar. De digitale representatie hiervan, noemt het RVO ook wel een referentieperceel. De landschapselementen in en binnen de buffer rond het perceel, komen terecht in de referentielaag landschapselementen. Niet tot de inhoud van het IMLE behoren de (niet-agrarische) landschapselementen
die buiten dit grongebied valt.


Modellering
-----------

Het IMLE hanteert het Metamodel voor Informatiemodellering [[MIM11]] voor de
modellering van het IMLE. Hierbij hoort het invullen van MIM metagegevens. Het IMLE sluit verder aan bij het het Basismodel Geo-informatie [[NEN3610]] op het gebied van semantiek. NEN 3610:2011 conformeert zich aan de [[ISO19108-2005]] en [[ISO19118-2011]] standaarden voor
geo-informatie. Deze gelden daarom ook voor de IMLE.


