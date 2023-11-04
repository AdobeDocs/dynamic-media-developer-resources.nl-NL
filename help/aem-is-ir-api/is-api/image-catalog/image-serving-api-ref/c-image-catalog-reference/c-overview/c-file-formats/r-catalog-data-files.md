---
description: Gegevensbestanden van catalogi kunnen elke naam en elk achtervoegsel van het bestand hebben (behalve .ini). Ze kunnen eenvoudig worden onderhouden met toepassingen die door tabs gescheiden tekstgegevensbestanden ondersteunen, zoals Microsoft Excel en Access.
solution: Experience Manager
title: Catalogusgegevensbestanden
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4aa20abe-4f84-470b-b5a1-3d9246ab1792
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Catalogusgegevensbestanden{#catalog-data-files}

Gegevensbestanden van catalogi kunnen elke naam en elk achtervoegsel van het bestand hebben (behalve .ini). Ze kunnen eenvoudig worden onderhouden met toepassingen die door tabs gescheiden tekstgegevensbestanden ondersteunen, zoals Microsoft Excel en Access.

In wezen bestaat een catalogusgegevensbestand in een tweedimensionale tabel uit een headerrecord die de gegevenskolommen en elk gewenst aantal gegevensrecords (rijen) identificeert. Velden in zowel koptekst- als gegevensrecords worden gescheiden door één veld `<TAB>` tekens. Records worden gescheiden door één record `<CR>` (ASCII-code `0xD`), één `<LF>` (ASCII-code `0xA`), of een `<CR><LF>` paar.

De headerrecord moet de exacte namen voor elk gegevensveld bevatten. Lege velden zijn niet toegestaan in de koptekstrij. Namen van gegevensvelden zijn niet hoofdlettergevoelig. Alle veldnamen moeten uniek zijn.

Spaties kunnen niet worden gebruikt als veldscheidingstekens. Er zijn geen spaties toegestaan in de koptekstrecord. In gegevensrecords worden spaties aan het begin of einde van een gegevensveld beschouwd als onderdeel van dat gegevensveld.

In de gegevensrecords, twee naast elkaar `<TAB>` tekens duiden op een leeg veld. Lege velden kunnen standaardwaarden overnemen van de cataloguskenmerken of van de standaardinstellingen van de server.

Gegevensvelden kunnen eventueel worden ingesloten door dubbele aanhalingstekens. Zij mogen geen `<CR>`, `<LF>`, of `<TAB>` tekens, tenzij de gegevenswaarde van het type tekst is en door dubbele aanhalingstekens wordt ingesloten. Gegevensvelden mogen niet via HTTP zijn gecodeerd.

Meerdere gegevenswaarden in hetzelfde veld worden gescheiden door komma&#39;s, tenzij anders aangegeven.

Kolommen waarvan de naam begint met &quot;.&quot; worden genegeerd. Hierdoor kunnen gegevens in afbeeldingscatalogi worden opgeslagen, wat niet interessant is voor beeldbewerking. Kolommen met onbekende koptekstnamen worden genegeerd en er wordt een waarschuwing naar het logbestand geschreven.

Veldnamen kunnen bestaan uit elke combinatie van ASCII-letters, -cijfers en &quot;-&quot; en &quot;_&quot;.

Een of meer kolommen kunnen worden gebruikt als indexsleutels. Als dezelfde sleutel meerdere keren voorkomt in hetzelfde gegevensbestand, heeft de latere instantie voorrang.
