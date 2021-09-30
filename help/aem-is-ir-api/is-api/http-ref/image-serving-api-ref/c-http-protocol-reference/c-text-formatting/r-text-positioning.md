---
title: Tekstpositionering
description: De renderer text= positioneert tekst fundamenteel verschillend dan de renderer textPs= wanneer toegepast op presize lagen (d.w.z. wanneer size= ook wordt gespecificeerd).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 092444bf-9964-4d97-b06e-3add033da284
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# Tekstpositionering{#text-positioning}

De renderer `text=` positioneert tekst fundamenteel verschillend dan de renderer textPs= wanneer toegepast op presize lagen (d.w.z. wanneer size= ook wordt gespecificeerd).

Zelf formaat `text=`en `textPs=` lagen hebben gelijkaardige verschijning en het plaatsen.

`textPs=` lijnt de bovenkant van de karaktercel met de bovenkant van het tekstvakje (veronderstellend `\vertalt`) uit, zelfs als het in delen van de teruggegeven tekstglyphs die zich gedeeltelijk buiten de grens van het tekstvakje uitbreiden. Gegenereerde glyphs van bepaalde lettertypen kunnen ook iets buiten de linker- en rechterrand van het tekstvak uitsteken. Voor toepassingen die vereisen dat alle gerenderde tekst zich binnen de laagrechthoek moet bevinden, kunnen de RTF `\marg*` bevelen of `textFlowPath=` worden gebruikt om het tekst terug te geven gebied aan te passen.

Met `text=` daarentegen wordt de gerenderde tekst naar wens verschoven en wordt gegarandeerd dat alle gerenderde glyphs volledig binnen het opgegeven tekstvak passen.

Hoewel `text=` iets gemakkelijker te gebruiken is voor eenvoudige toepassingen, biedt `textPs=` nauwkeurige positionering onafhankelijk van lettertypen en teksteffecten.

## Voorbeelden {#section-1b6bdf2ea34447528188ae4e1430ee71}

De volgende voorbeelden zijn voor tekst van vooraf formaat. Het gedrag voor tekst op zichzelf wijzigen is anders.

** `Text=` biedt altijd een smalle marge bovenaan:**

![Voorbeeld van tekstpositionering van één afbeelding](assets/tp01.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20Normal%20Normal`

** `textPs=` geeft de tekst strak uitgelijnd op de bovenkant van het tekstvak. Dit leidt tot een kleine bijsnijding, zelfs voor gewone lettertypen zoals Arial®:**

![Voorbeeld van tekstpositionering van twee afbeeldingen](assets/tp02.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20Normal%20Normal`

** `text=` verplaatst de weergegeven tekst automatisch omlaag om bijsnijden te voorkomen:**

![Voorbeeld van tekstpositionering van drie afbeeldingen](assets/tp03.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20{\up20Raised%20}Normal`

** `textPs=` verplaatst geen tekst met verheven gedeelten. Dit leidt tot aanzienlijk bijsnijden als de tekst zich op laag 0 bevindt:**

![Voorbeeld van tekstpositionering van vier afbeeldingen](assets/tp04.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20{\up20Raised%20}Normal`

**Een marge van 10 pt (200 twips) boven rendert deze tekst zonder bijsnijden:**

![Voorbeeld van tekstpositionering van vijf afbeeldingen](assets/tp05.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\margt200\fs40Normal%20{\up20Raised}%20Normal`

**Gerenderde glyphs van bepaalde scriptlettertypen kunnen aanzienlijk buiten het tekstvak komen:**

![Voorbeeld van tekstpositionering zes afbeeldingen](assets/tp06.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs={\fonttbl{\f1\fcharset0%20FluffyFont;}}\f1\fs88%20fluffy%20font%20problems`
