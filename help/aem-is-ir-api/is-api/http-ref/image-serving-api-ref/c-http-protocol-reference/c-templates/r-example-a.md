---
title: Voorbeeld A
description: Maak een sjabloon met een vaste grootte met een statische achtergrondafbeelding, een variabele afbeelding die links op de achtergrond wordt uitgelijnd en wordt geschaald tot maximaal 80% van de breedte en hoogte van de achtergrond. Tot slot één tekstlaag met verticale tekst gecentreerd op de rechterrand van het canvas.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7f731b41-994d-4f1d-b42d-e14db47e4d6c
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 0%

---

# Voorbeeld A{#example-a}

Maak een sjabloon met een vaste grootte met een statische achtergrondafbeelding, een variabele afbeelding die links op de achtergrond wordt uitgelijnd en wordt geschaald tot maximaal 80% van de breedte en hoogte van de achtergrond. Tot slot één tekstlaag met verticale tekst gecentreerd op de rechterrand van het canvas.

![Een voorbeeld van een afbeelding bekijken](assets/examplea.png)

## De sjabloonrecord {#section-32f54710593e438fa0622224c89380af}

Object invoegen

<table id="simpletable_97ECA49445634F59B3F1D100412EFC70"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalogus::Id </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> myTemplate1 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalogus::Modifier </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> src=backgroundImage&amp;size=1000,1000&amp;originN=0,0&amp; layer=1&amp;src=$object$&amp;size=800,800&amp;originN=-0.5,0&amp;posN=-0.5,0&amp; layer=2&amp;$text=layer&amp;2+text+goes+here text=rtf...$text$..rtf-encoding&amp;rotate=-90&amp;originN=0.5,0&amp;posN=0.5,0 </span> </p> </td> 
 </tr> 
</table>

De `origin=` De waarden van alle lagen worden uitdrukkelijk gespecificeerd in het malplaatje om het plaatsen en de groepering van de lagen strikt te controleren. Elke oorsprong van de laag wordt ingesteld zodat deze overeenkomt met de gewenste uitlijning voor die laag. De `origin=` voor de achtergrond (laag 0) is ingesteld op het middelpunt; deze waarde is arbitrair omdat de achtergrondafbeelding bij uitvoering niet verandert; alle waarden voor de oorsprong van laag 0 kunnen worden gebruikt.

De `pos=` de waarden verstrekken de noodzakelijke compensatie tussen de punten van de laagoorsprong, om de gewenste laag te bereiken plaatsend.

Het anker voor de afbeelding van laag 1 wordt links in het midden geplaatst, met de `pos=` waarde. Met deze instelling wordt de achtergrondafbeelding en de afbeelding met laag 1 links uitgelijnd, ongeacht de hoogte-breedteverhouding van de afbeelding met laag 1.

Op dezelfde manier wordt het anker voor de tekstlaag gepositioneerd in het rechtermidden van het tekstvak met het automatische formaat, met de optie `pos=` waarde. Met deze instelling wordt de gewenste rechts-gecentreerde uitlijning bereikt voor de geroteerde tekst, onafhankelijk van de tekengrootte en tekenreekslengte.

De werkelijke weergavetekst wordt tijdens runtime weergegeven, zodat een variabele wordt gebruikt om de tekst te scheiden van het omhulsel voor RTF-opmaak. De standaardvariabele `$object` wordt gebruikt voor de afbeelding van laag 1. Met deze variabele kunt u deze afbeelding opgeven in het aanvraagpad.

Elke afbeelding kan worden gebruikt voor de achtergrondafbeelding en de afbeelding van laag 1. Als de achtergrondafbeelding een masker heeft, worden de niet-gemaskerde gebieden gevuld met de standaardachtergrondkleur ( `attribute::BkgColor`), of links transparant wanneer `fmt=png-alpha` of `fmt=tif-alpha`. Als de achtergrondafbeelding een niet-vierkante hoogte-breedteverhouding heeft, wordt deze gecentreerd in de antwoordafbeelding en wordt de extra ruimte gevuld met `attribute::BkgColor`. Als de afbeelding van laag 1 alpha-gegevens of een masker bevat, blijft de achtergrondafbeelding (of achtergrondkleur) zichtbaar in de transparante gebieden. Als de afbeelding geen masker heeft, wordt de volledige toegewezen rechthoek gevuld.

## De sjabloon gebruiken {#section-3e04eedc268c482db5a8cfc662c0f327}

` http:// *`server`*/myRootId/anotherImage?template=myTemplate1&$text=about+the+image`

In de volgende afbeelding ziet u het samengestelde resultaat voor verschillende hoogte-breedteverhoudingen van de afbeelding met laag 1 en verschillende tekstreeksen.

![Voorbeeld van een afbeelding met een samengesteld resultaat](assets/exampleausing.png)
