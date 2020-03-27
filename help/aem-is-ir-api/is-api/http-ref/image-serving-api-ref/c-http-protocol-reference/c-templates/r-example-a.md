---
description: Maak een sjabloon met een vaste grootte met een statische achtergrondafbeelding, een variabele afbeelding die links op de achtergrond wordt uitgelijnd en wordt geschaald tot maximaal 80% van de breedte en hoogte van de achtergrond, en een tekstlaag met verticale tekst gecentreerd op de rechterrand van het canvas.
seo-description: Maak een sjabloon met een vaste grootte met een statische achtergrondafbeelding, een variabele afbeelding die links op de achtergrond wordt uitgelijnd en wordt geschaald tot maximaal 80% van de breedte en hoogte van de achtergrond, en een tekstlaag met verticale tekst gecentreerd op de rechterrand van het canvas.
seo-title: Voorbeeld A
solution: Experience Manager
title: Voorbeeld A
topic: Scene7 Image Serving - Image Rendering API
uuid: c250dbc8-1e32-46b8-ba55-c1fb0ae62695
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Voorbeeld A{#example-a}

Maak een sjabloon met een vaste grootte met een statische achtergrondafbeelding, een variabele afbeelding die links op de achtergrond wordt uitgelijnd en wordt geschaald tot maximaal 80% van de breedte en hoogte van de achtergrond, en een tekstlaag met verticale tekst gecentreerd op de rechterrand van het canvas.

![](assets/examplea.png)

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

De `origin=` waarden van alle lagen worden uitdrukkelijk gespecificeerd in het malplaatje om het plaatsen en de groepering van de lagen strikt te controleren. Elke oorsprong van de laag wordt ingesteld zodat deze overeenkomt met de gewenste uitlijning voor die laag. De `origin=` achtergrondlaag (laag 0) wordt op het middelpunt ingesteld; dit willekeurig is omdat de achtergrondafbeelding bij uitvoering niet verandert; alle waarden voor de oorsprong van laag 0 kunnen worden gebruikt.

De `pos=` waarden zorgen voor de noodzakelijke verschuivingen tussen de oorsprongpunten van de laag om de gewenste laagpositionering te bereiken.

Het anker voor de afbeelding van laag 1 wordt links in het midden geplaatst. in combinatie met de `pos=` waarde, bereikt u hiermee de uitlijning naar links tussen de achtergrond en de afbeelding met laag 1, ongeacht de hoogte-breedteverhouding van de afbeelding met laag 1.

Het anker voor de tekstlaag wordt op dezelfde manier in het midden van het tekstvak met automatische grootte geplaatst. In combinatie met pos= bereikt u hiermee de gewenste uitlijning naar rechts voor de geroteerde tekst, onafhankelijk van tekengrootte en tekenreekslengte.

De werkelijke weergavetekst wordt tijdens runtime weergegeven, zodat een variabele wordt gebruikt om de tekst te scheiden van het omhulsel voor RTF-opmaak. Wij gebruiken de standaardvariabele `$object` voor laag 1 beeld. Hierdoor kan deze afbeelding in het aanvraagpad worden opgegeven.

Elke afbeelding kan worden gebruikt voor de achtergrondafbeelding en de afbeelding van laag 1. Als de achtergrondafbeelding een masker heeft, worden de niet-gemaskerde gebieden gevuld met de standaardachtergrondkleur ( `attribute::BkgColor`), of wordt deze transparant gemaakt wanneer `fmt=png-alpha` of `fmt=tif-alpha`. Als de achtergrondafbeelding een niet-vierkante hoogte-breedteverhouding heeft, wordt deze gecentreerd in de antwoordafbeelding en wordt de extra ruimte gevuld met `attribute::BkgColor`. Als de afbeelding van laag 1 alpha-gegevens of een masker bevat, blijft de achtergrondafbeelding (of de achtergrondkleur) zichtbaar in de transparante gebieden. Als de afbeelding geen masker heeft, wordt de volledige toegewezen rechthoek gevuld.

## De sjabloon gebruiken {#section-3e04eedc268c482db5a8cfc662c0f327}

` http:// *`server`*/myRootId/anotherImage?template=myTemplate1&$text=about+the+image`

In de volgende afbeelding ziet u het samengestelde resultaat voor verschillende hoogte-breedteverhoudingen van de afbeelding met laag 1 en verschillende tekstreeksen.

![](assets/exampleausing.png)

