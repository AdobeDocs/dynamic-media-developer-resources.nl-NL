---
description: Gegevensbestanden van catalogi kunnen elke naam en elk achtervoegsel van het bestand hebben (behalve .ini). Ze kunnen eenvoudig worden onderhouden met toepassingen die door tabs gescheiden tekstgegevensbestanden ondersteunen, zoals Microsoft Excel en Access.
seo-description: Gegevensbestanden van catalogi kunnen elke naam en elk achtervoegsel van het bestand hebben (behalve .ini). Ze kunnen eenvoudig worden onderhouden met toepassingen die door tabs gescheiden tekstgegevensbestanden ondersteunen, zoals Microsoft Excel en Access.
seo-title: Catalogusgegevensbestanden
solution: Experience Manager
title: Catalogusgegevensbestanden
topic: Scene7 Image Serving - Image Rendering API
uuid: 0f66e2fe-5b8a-43d3-bf2e-8dd79da6a581
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Catalogusgegevensbestanden{#catalog-data-files}

Gegevensbestanden van catalogi kunnen elke naam en elk achtervoegsel van het bestand hebben (behalve .ini). Ze kunnen eenvoudig worden onderhouden met toepassingen die door tabs gescheiden tekstgegevensbestanden ondersteunen, zoals Microsoft Excel en Access.

In wezen bestaat een catalogusgegevensbestand in een tweedimensionale tabel uit een headerrecord die de gegevenskolommen en elk gewenst aantal gegevensrecords (rijen) identificeert. Velden in zowel koptekst- als gegevensrecords worden gescheiden door enkele `<TAB>` tekens. Records worden gescheiden door één `<CR>` (ASCII-code `0xD`), één `<LF>` (ASCII-code `0xA`) of `<CR><LF>` paar.

De headerrecord moet de exacte namen voor elk gegevensveld bevatten. Lege velden zijn niet toegestaan in de koptekstrij. Namen van gegevensvelden zijn niet hoofdlettergevoelig. Alle veldnamen moeten uniek zijn.

Spaties kunnen niet worden gebruikt als veldscheidingstekens. Er zijn geen spaties toegestaan in de koptekstrecord. In gegevensrecords worden spaties aan het begin of einde van een gegevensveld beschouwd als onderdeel van dat gegevensveld.

In de gegevensrecords geven twee aangrenzende `<TAB>` tekens een leeg veld aan. Lege velden kunnen standaardwaarden overnemen van de cataloguskenmerken of van de standaardinstellingen van de server.

Gegevensvelden kunnen eventueel worden ingesloten door dubbele aanhalingstekens. Ze mogen geen `<CR>`, `<LF>`of `<TAB>` tekens bevatten, tenzij de gegevenswaarde van het type tekst is en door dubbele aanhalingstekens wordt ingesloten. Gegevensvelden mogen niet via HTTP zijn gecodeerd.

Meerdere gegevenswaarden in hetzelfde veld worden gescheiden door komma&#39;s, tenzij anders aangegeven.

Kolommen waarvan de naam begint met &quot;.&quot; worden genegeerd. Hierdoor kunnen gegevens in afbeeldingscatalogi worden opgeslagen, wat niet interessant is voor beeldbewerking. Kolommen met onbekende koptekstnamen worden genegeerd en er wordt een waarschuwing naar het logbestand geschreven.

Veldnamen kunnen bestaan uit elke combinatie van ASCII-letters, -cijfers en &quot;-&quot; en &quot;_&quot;.

Een of meer kolommen kunnen worden gebruikt als indexsleutels. Als dezelfde sleutel meerdere keren voorkomt in hetzelfde gegevensbestand, heeft de latere instantie voorrang.
