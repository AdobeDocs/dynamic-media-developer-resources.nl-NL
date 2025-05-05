---
title: Tekstpositionering
description: De renderer text= positioneert tekst fundamenteel verschillend van textPs= renderer wanneer toegepast op presize lagen (namelijk wanneer size= ook wordt gespecificeerd).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 092444bf-9964-4d97-b06e-3add033da284
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---

# Tekstpositionering{#text-positioning}

De `text=` renderer plaatst tekst fundamenteel verschillend van textPs= renderer wanneer toegepast op presize lagen (namelijk wanneer size= ook wordt gespecificeerd).

Zelfaanpassing `text=`en `textPs=` lagen hebben een vergelijkbare vormgeving en positie.

De `textPs=` Hiermee wordt de bovenkant van de tekencel uitgelijnd met de bovenkant van het tekstvak (uitgaande van `\vertalt`), zelfs als het resultaat is dat delen van de weergegeven tekstglyphs zich gedeeltelijk buiten de grens van het tekstvak uitstrekken. Gegenereerde glyphs van bepaalde lettertypen kunnen ook iets buiten de linker- en rechterrand van het tekstvak uitsteken. Voor toepassingen waarbij alle gerenderde tekst zich in de laagrechthoek moet bevinden, wordt de RTF `\marg*` opdrachten of `textFlowPath=` U kunt het tekstrendergebied aanpassen.

In tegenstelling tot `text=` Hiermee wordt de gerenderde tekst zo nodig verplaatst en wordt gegarandeerd dat alle gerenderde glyphs volledig binnen het opgegeven tekstvak passen.

while `text=` is wellicht iets gemakkelijker te gebruiken voor eenvoudige toepassingen, `textPs=` biedt nauwkeurige positionering, onafhankelijk van lettertypen en teksteffecten.

## Voorbeelden {#section-1b6bdf2ea34447528188ae4e1430ee71}

De volgende voorbeelden zijn voor tekst van vooraf formaat. Het gedrag voor tekst op zichzelf wijzigen is anders.

**&#x200B; `Text=` biedt altijd een smalle marge bovenaan:**

![Voorbeeld van tekstpositionering van één afbeelding](assets/tp01.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20Normal%20Normal`

**&#x200B; `textPs=` Hiermee wordt tekst strak uitgelijnd op de bovenkant van het tekstvak, wat resulteert in een kleine bijgesneden tekst, zelfs voor algemene lettertypen zoals Arial®:**

![Voorbeeld van tekstpositionering van twee afbeeldingen](assets/tp02.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20Normal%20Normal`

**&#x200B; `text=` Hiermee wordt gerenderde tekst automatisch omlaag verplaatst om bijsnijden te voorkomen:**

![Voorbeeld van tekstpositionering van drie afbeeldingen](assets/tp03.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20{\up20Raised%20}Normal`

**&#x200B; `textPs=` verplaatst geen tekst die verhoogde gedeelten bevat, wat resulteert in aanzienlijk bijsnijden als de tekst zich op laag 0 bevindt:**

![Voorbeeld van tekstpositionering van vier afbeeldingen](assets/tp04.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20{\up20Raised%20}Normal`

**Een marge van 10 pt (200 twips) boven rendert deze tekst zonder bijsnijden:**

![Voorbeeld van tekstpositionering van vijf afbeeldingen](assets/tp05.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\margt200\fs40Normal%20{\up20Raised}%20Normal`

**Gerenderde glyphs van bepaalde scriptlettertypen kunnen aanzienlijk buiten het tekstvak komen:**

![Voorbeeld van tekstpositionering zes afbeeldingen](assets/tp06.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs={\fonttbl{\f1\fcharset0%20FluffyFont;}}\f1\fs88%20fluffy%20font%20problems`
