---
description: Gegevensbestanden van catalogi kunnen elke naam en elk achtervoegsel van het bestand hebben (behalve .ini).
seo-description: Gegevensbestanden van catalogi kunnen elke naam en elk achtervoegsel van het bestand hebben (behalve .ini).
seo-title: Catalogusgegevensbestanden
solution: Experience Manager
title: Catalogusgegevensbestanden
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 33d991d6-5aa7-4cc6-88d4-10c4bb83d786
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---


# Catalogusgegevensbestanden{#catalog-data-files}

Gegevensbestanden van catalogi kunnen elke naam en elk achtervoegsel van het bestand hebben (behalve .ini).

U kunt catalogusgegevensbestanden eenvoudig onderhouden met toepassingen die door tabs gescheiden tekstgegevensbestanden, zoals Microsoft Excel en Access, ondersteunen.

In wezen bestaat een catalogusgegevensbestand uit een koptekstrecord waarin de gegevenskolommen en een willekeurig aantal gegevensrecords (rijen) worden geïdentificeerd. De gebieden in zowel kopbal als gegevensverslagen worden gescheiden door enige `<TAB>` karakters. Records worden gescheiden door één `<CR>` (ASCII-code 0xD), één `<LF>` (ASCII-code 0xA) of een `<CR><LF>`-paar.

De headerrecord moet de exacte namen voor elk gegevensveld bevatten. Lege velden zijn niet toegestaan in de koptekstrij. Namen van gegevensvelden zijn niet hoofdlettergevoelig. Alle veldnamen moeten uniek zijn.

In koptekst- en gegevensrecords is geen andere witruimte dan de `<TAB>`-veldscheidingstekens toegestaan.

In de gegevensrecords geven twee naast elkaar gelegen `<TAB>` tekens een leeg veld aan. Lege velden nemen de standaardwaarden over van de cataloguskenmerken of van de standaardinstellingen van de server.

Gegevensvelden mogen geen `<CR>`-, `<LF>`- of `<TAB>`-tekens bevatten, tenzij de gegevenswaarde van het type tekst is en door enkele of dubbele aanhalingstekens wordt ingesloten. Gegevensvelden mogen niet via HTTP zijn gecodeerd.

Meerdere gegevenswaarden in hetzelfde veld worden gescheiden door komma&#39;s (&#39;,&#39;), tenzij anders aangegeven.

Kolommen waarvan de naam begint met &#39;.&#39; worden genegeerd; Hierdoor kunnen gegevens worden opgeslagen in materiaalcatalogi die niet van belang zijn voor het renderen van afbeeldingen. Kolommen met onbekende koptekstnamen worden genegeerd en er wordt een waarschuwing naar het logbestand geschreven.

Veldnamen kunnen bestaan uit elke combinatie van ASCII-letters, -cijfers en &quot;-&quot; en &quot;_&quot;.

Een of meer kolommen kunnen worden gebruikt als indexsleutels. Als dezelfde sleutel meerdere keren voorkomt in hetzelfde gegevensbestand, heeft de latere instantie voorrang.
