---
description: Eindweergaverechthoek. Hiermee kunt u de uiteindelijke afbeelding van de weergave splitsen in verschillende stroken of tegels, die afzonderlijk kunnen worden geleverd en naadloos kunnen worden samengevoegd door de client, zonder artefacten langs de randen.
seo-description: Eindweergaverechthoek. Hiermee kunt u de uiteindelijke afbeelding van de weergave splitsen in verschillende stroken of tegels, die afzonderlijk kunnen worden geleverd en naadloos kunnen worden samengevoegd door de client, zonder artefacten langs de randen.
seo-title: rect
solution: Experience Manager
title: rect
topic: Dynamic Media Image Serving - Image Rendering API
uuid: c4830fc5-d102-4789-8753-0a660d4a557e
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---


# rect{#rect}

Eindweergaverechthoek. Hiermee kunt u de uiteindelijke afbeelding van de weergave splitsen in verschillende stroken of tegels, die afzonderlijk kunnen worden geleverd en naadloos kunnen worden samengevoegd door de client, zonder artefacten langs de randen.

`rect= *``*, *``*[, *`coördinaatschaal`*]`

<table id="simpletable_69D112F85FA24EFCA727B398DC8ED699"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p> </td> 
  <td class="stentry"> <p>De pixelverschuiving van de linkerbovenhoek van de weergaveafbeelding naar de linkerbovenhoek van de weergaverechthoek (int, int), uitgedrukt in pixels, nadat <span class="varname"> scale</span> is toegepast. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> size</span> </p></td> 
  <td class="stentry"> <p>Grootte van de ROI in pixels (int, int). Hiermee geeft u de grootte van de antwoordafbeelding op. De afbeelding wordt gevuld met <span class="codeph"> bgc=</span> in gebieden die niet door de weergaveafbeelding worden gedekt (of links transparant, als <span class="codeph"> fmt=*-alpha</span> aanwezig is in de aanvraag). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> schalen</span> </p></td> 
  <td class="stentry"> <p>Schaalfactor (reëel). Bij waarden kleiner dan 1,0 neemt de resolutie af en bij waarden groter dan 1,0 neemt de resolutie toe. </p></td> 
 </tr> 
</table>

Met deze opdracht kunnen via HTTP grote afbeeldingen worden geleverd die anders de maximale grootte overschrijden die is geconfigureerd met `attribute::MaxPix`.

>[!NOTE]
>
>Als u JPEG-compressie gebruikt, krijgt u het beste resultaat als de strip- of tegelgrootte een veelvoud is van de grootte van het JPEG-coderingstitel (16 x 16 pixels).

## Voorbeeld {#section-932fcfcb41d74a29bc929e4430c49601}

Scheid een afdrukbare CMYK-afbeelding in verschillende strepen met volledige resolutie om de bestandsgrootte van het downloadbestand te beperken. Als wij om een aaneengesloten beeld zouden verzoeken:

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&fmt=tif&icc=WebCoated`

Eerst wordt relevante informatie over de afbeelding verkregen:

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&req=props`

De tekstreactie bevat de volgende eigenschappen:

`image.width=2000 image.height=2400 image.version=37JK6NTvpvC42F5gOuLEVY`

Op basis van deze informatie kiezen we voor vier stroken van 600 x 2000 pixels. De opdracht `rect=` wordt gebruikt om de stripgrootten en -posities te beschrijven.

Aangezien deze afbeelding regelmatig wordt gewijzigd, gebruiken we de opdracht `id=` om de kans te minimaliseren dat we terechtkomen met een of meer stroken van een oudere versie van de afbeelding die mogelijk in de cache zijn geplaatst op een CDN- of proxyserver. De waarde van het `image.version` bezit wordt gebruikt voor dit doel.

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,0,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,600,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1200,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1800,2000,600`

## Eigenschappen {#section-aae223cee13e46d38b74680c048d945b}

Kenmerk weergeven. Is van toepassing ongeacht de huidige laaginstelling.

Om het even welke gebieden van ROI die buiten het meningsbeeld uitbreiden worden opgevuld met `bgc=`.

Belangrijk `rect=` wordt toegepast *na* definitieve schaling en aanpassing met `scl=`, `wid=`, `hei=`, `fit=`, `rgn=` en `align=`.

## Standaard {#section-b296d3bbfb19441f87137a452b70f19a}

Gehele, ongewijzigde weergaveafbeelding ( `rect=0,0,width,height,1.0`).

## Zie ook {#section-74015202c0c545ec82aec614d74b4bbd}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) ,  [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac),  [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47),  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f)  [ ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)  [align=, fit=,rgn=,attribute:MaxPix,id=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0)
