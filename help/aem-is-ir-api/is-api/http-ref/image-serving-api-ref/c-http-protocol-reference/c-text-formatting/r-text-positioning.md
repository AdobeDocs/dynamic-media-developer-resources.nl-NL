---
description: De renderer text= positioneert tekst fundamenteel verschillend dan de renderer textPs= wanneer toegepast op presize lagen (d.w.z. wanneer size= ook wordt gespecificeerd).
seo-description: De renderer text= positioneert tekst fundamenteel verschillend dan de renderer textPs= wanneer toegepast op presize lagen (d.w.z. wanneer size= ook wordt gespecificeerd).
seo-title: Tekstpositionering
solution: Experience Manager
title: Tekstpositionering
topic: Scene7 Image Serving - Image Rendering API
uuid: 77289c50-2f3a-4486-8274-eecfd6e5452f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Tekstpositionering{#text-positioning}

De renderer text= positioneert tekst fundamenteel verschillend dan de renderer textPs= wanneer toegepast op presize lagen (d.w.z. wanneer size= ook wordt gespecificeerd).

Zelf vergroten/verkleinen `text=`en `textPs=` lagen hebben een vergelijkbare vormgeving en positionering.

`textPs=` Hiermee wordt de bovenkant van de tekencel uitgelijnd op de bovenkant van het tekstvak ( `\vertalt`wordt ervan uitgegaan), zelfs als dit ertoe leidt dat delen van de weergegeven tekstglyphs zich gedeeltelijk buiten de grens van het tekstvak uitstrekken. Gegenereerde glyphs van bepaalde lettertypen kunnen ook iets buiten de linker- en rechterrand van het tekstvak uitsteken. Voor toepassingen die vereisen dat alle gerenderde tekst zich binnen de laagrechthoek moet bevinden, `\marg*` beveelt RTF of `textFlowPath=` kan worden gebruikt om het tekstrendergebied aan te passen.

De gerenderde tekst wordt daarentegen zo nodig verschoven en er wordt voor gezorgd dat alle weergegeven glyphs volledig binnen het opgegeven tekstvak passen. `text=`

Hoewel u deze functie iets eenvoudiger `text=` kunt gebruiken voor eenvoudige toepassingen, `textPs=` biedt deze functie nauwkeurige positionering, onafhankelijk van lettertypen en teksteffecten.

## Voorbeelden {#section-1b6bdf2ea34447528188ae4e1430ee71}

De volgende voorbeelden zijn voor tekst van vooraf formaat. Het gedrag voor tekst op zichzelf wijzigen is anders.

** `Text=` biedt altijd een smalle marge bovenaan:**

![](assets/tp01.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20Normal%20Normal`

** `textPs=` zorgt ervoor dat de tekst strak wordt uitgelijnd op de bovenzijde van het tekstvak. Dit kan resulteren in een kleine bijsnijding, zelfs voor gewone lettertypen zoals Arial:**

![](assets/tp02.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20Normal%20Normal`

** `text=` wordt weergegeven tekst automatisch omlaag verplaatst om uitknippen te voorkomen:**

![](assets/tp03.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20{\up20Raised%20}Normal`

** `textPs=` wordt geen tekst met verhoogde gedeelten verplaatst, wat resulteert in aanzienlijk bijsnijden als de tekst zich op laag 0 bevindt:**

![](assets/tp04.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20{\up20Raised%20}Normal`

**Een marge van 10 pt (200 twips) boven rendert deze tekst zonder bijsnijden:**

![](assets/tp05.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\margt200\fs40Normal%20{\up20Raised}%20Normal`

**Gerenderde glyphs van bepaalde scriptlettertypen kunnen aanzienlijk buiten het tekstvak komen:**

![](assets/tp06.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs={\fonttbl{\f1\fcharset0%20FluffyFont;}}\f1\fs88%20fluffy%20font%20problems`
