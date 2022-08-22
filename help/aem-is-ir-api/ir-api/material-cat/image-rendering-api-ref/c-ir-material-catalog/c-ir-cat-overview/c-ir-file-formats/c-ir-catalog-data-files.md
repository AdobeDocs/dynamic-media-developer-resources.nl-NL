---
title: Catalogusgegevensbestanden
description: Gegevensbestanden van catalogi kunnen elke naam en elk achtervoegsel van het bestand hebben (behalve .ini).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1fb91795-f699-40b4-a6bc-6eab3e1ecd1d
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# Catalogusgegevensbestanden{#catalog-data-files}

Gegevensbestanden van Catalog kunnen elke naam en elk achtervoegsel van het bestand hebben (behalve `.ini`).

U kunt catalogusgegevensbestanden eenvoudig onderhouden met toepassingen die door tabs gescheiden tekstgegevensbestanden ondersteunen, zoals Microsoft® Excel en Access.

In wezen bestaat een catalogusgegevensbestand uit een koptekstrecord waarin de gegevenskolommen en een willekeurig aantal gegevensrecords (rijen) worden geïdentificeerd. Velden in zowel koptekst- als gegevensrecords worden gescheiden door één veld `<TAB>` tekens. Records worden gescheiden door één record `<CR>` (ASCII-code) `0xD`), één `<LF>` (ASCII-code) `0xA`), of een `<CR><LF>` paar.

De headerrecord moet de exacte namen voor elk gegevensveld bevatten. Lege velden zijn niet toegestaan in de koptekstrij. Namen van gegevensvelden zijn niet hoofdlettergevoelig. Alle veldnamen moeten uniek zijn.

Geen andere witruimte dan de `<TAB>` veldscheidingstekens zijn toegestaan in koptekst- en gegevensrecords.

In de gegevensrecords, twee naast elkaar `<TAB>` tekens duiden op een leeg veld. Lege velden nemen de standaardwaarden over van de cataloguskenmerken of van de standaardinstellingen van de server.

Gegevensvelden mogen geen `<CR>`, `<LF>`, of `<TAB>` tekens, tenzij de gegevenswaarde van het type tekst is en door enkele of dubbele aanhalingstekens wordt ingesloten. Codeer gegevensvelden niet via HTTP.

Meerdere gegevenswaarden in hetzelfde veld worden gescheiden door komma&#39;s (&#39;,&#39;), tenzij anders aangegeven.

Kolommen waarvan de naam begint met &#39;.&#39; worden genegeerd; Hierdoor kunnen gegevens worden opgeslagen in materiaalcatalogi die niet van belang zijn voor het renderen van afbeeldingen. Kolommen met onbekende koptekstnamen worden genegeerd en er wordt een waarschuwing naar het logbestand geschreven.

Veldnamen kunnen bestaan uit elke combinatie van ASCII-letters, -cijfers en &quot;-&quot; en &quot;_&quot;.

Een of meer kolommen kunnen worden gebruikt als indextoetsen. Als dezelfde sleutel meerdere keren voorkomt in hetzelfde gegevensbestand, heeft de latere instantie voorrang.
