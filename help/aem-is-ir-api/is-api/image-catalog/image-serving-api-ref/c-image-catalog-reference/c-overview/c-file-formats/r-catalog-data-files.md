---
description: Gegevensbestanden van catalogi kunnen elke naam en elk achtervoegsel van het bestand hebben (behalve .ini). Ze kunnen eenvoudig worden onderhouden met toepassingen die door tabs gescheiden tekstgegevensbestanden ondersteunen, zoals Microsoft Excel en Access.
solution: Experience Manager
title: Catalogusgegevensbestanden
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 4aa20abe-4f84-470b-b5a1-3d9246ab1792
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 0%

---

# Catalogusgegevensbestanden{#catalog-data-files}

Gegevensbestanden van catalogi kunnen elke naam en elk achtervoegsel van het bestand hebben (behalve .ini). Ze kunnen eenvoudig worden onderhouden met toepassingen die door tabs gescheiden tekstgegevensbestanden ondersteunen, zoals Microsoft Excel en Access.

In wezen bestaat een catalogusgegevensbestand in een tweedimensionale tabel uit een headerrecord die de gegevenskolommen en elk gewenst aantal gegevensrecords (rijen) identificeert. De gebieden in zowel kopbal als gegevensverslagen worden gescheiden door enige `<TAB>` karakters. Records worden gescheiden door één `<CR>` (ASCII-code `0xD`), één `<LF>` (ASCII-code `0xA`) of een `<CR><LF>`-paar.

De headerrecord moet de exacte namen voor elk gegevensveld bevatten. Lege velden zijn niet toegestaan in de koptekstrij. Namen van gegevensvelden zijn niet hoofdlettergevoelig. Alle veldnamen moeten uniek zijn.

Spaties kunnen niet worden gebruikt als veldscheidingstekens. Er zijn geen spaties toegestaan in de koptekstrecord. In gegevensrecords worden spaties aan het begin of einde van een gegevensveld beschouwd als onderdeel van dat gegevensveld.

In de gegevensrecords geven twee naast elkaar gelegen `<TAB>` tekens een leeg veld aan. Lege velden kunnen standaardwaarden overnemen van de cataloguskenmerken of van de standaardinstellingen van de server.

Gegevensvelden kunnen eventueel worden ingesloten door dubbele aanhalingstekens. Ze mogen geen `<CR>`-, `<LF>`- of `<TAB>`-tekens bevatten, tenzij de gegevenswaarde van het type tekst is en door dubbele aanhalingstekens wordt ingesloten. Gegevensvelden mogen niet via HTTP zijn gecodeerd.

Meerdere gegevenswaarden in hetzelfde veld worden gescheiden door komma&#39;s, tenzij anders aangegeven.

Kolommen waarvan de naam begint met &quot;.&quot; worden genegeerd. Hierdoor kunnen gegevens in afbeeldingscatalogi worden opgeslagen, wat niet interessant is voor beeldbewerking. Kolommen met onbekende koptekstnamen worden genegeerd en er wordt een waarschuwing naar het logbestand geschreven.

Veldnamen kunnen bestaan uit elke combinatie van ASCII-letters, -cijfers en &quot;-&quot; en &quot;_&quot;.

Een of meer kolommen kunnen worden gebruikt als indexsleutels. Als dezelfde sleutel meerdere keren voorkomt in hetzelfde gegevensbestand, heeft de latere instantie voorrang.
