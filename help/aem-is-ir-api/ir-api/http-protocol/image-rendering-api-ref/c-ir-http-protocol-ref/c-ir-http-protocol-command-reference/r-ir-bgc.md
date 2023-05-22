---
title: bgc
description: Achtergrondkleur. Hiermee geeft u de subtractieve kleur op voor verkleurbare structuren en afkortingen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9ac6517e-b9c3-48d9-97ac-d8aa65a8ba46
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 0%

---

# bgc {#bgc}

Achtergrondkleur. Hiermee geeft u de subtractieve kleur op voor verkleurbare structuren en afkortingen.

`bgc= *[!DNL color]*`

<table id="simpletable_131302355CAB4900A7B45FED903A1AAD" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p><span class="+ topic/keyword sw-d/varname varname"> kleur</span> </p> </td> 
  <td class="- topic/stentry stentry"> <p>RGB- of grijskleurwaarde. </p></td> 
 </tr> 
</table>

Het inkleuringsalgoritme voor het renderen van afbeeldingen is eenvoudig: de componentwaarden van `bgc=` worden afgetrokken van de waarden van de structuurpixels; `color=` wordt toegevoegd en ten slotte wordt het resultaat afgekapt aan `0,0,0` en `255,255,255`.

Voor het typische gebruik van textuurinkleuring, de waarde voor `bgc=` Dit kan de belangrijkste of dominante kleur in de structuurafbeelding zijn. Dynamic Media Image Authoring biedt halfautomatische gereedschappen waarmee u redelijke `bgc=` kleurwaarden uit structuurafbeeldingen.

Wanneer een structuurmateriaal wordt toegepast op een niet-tekentabel vignetobject, `bgc=` wordt toegepast als voorgrondkleur, indien `color=` is niet opgegeven.

## Eigenschappen {#section-b2db6f147d7f443ba9f671de04c2ef19}

Materiaalkenmerk. Genegeerd door effen kleuren en kastmaterialen.

## Standaard {#section-de10ef5985ee4ae1ba56d14ba8512b81}

`catalog::BaseColor` Als het materiaal op een catalogusitem is gebaseerd, anders `bgc=808080` (neutraal grijs).

## Voorbeeld {#section-bf5f0f296bc448ed9d5a84afabcf81e6}

Inkleuren van een kledingweefsel waarvan de textuur de dominante RGB kleur 120,34,193 heeft:

`…&src=fabrics/d213.jpg&res=40&bgc=120,34,193&color=140,95,100&…`

## Zie ook {#section-de9958dd63a742b4b5d780c59a57da33}

[catalogus::BaseColor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-basecolor.md#reference-5f02371b1d8e444ab12d2614d9792de8) , [color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa)
