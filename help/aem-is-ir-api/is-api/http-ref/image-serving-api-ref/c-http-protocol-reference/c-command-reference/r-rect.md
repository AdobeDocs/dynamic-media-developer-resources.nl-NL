---
description: Eindweergaverechthoek. Hiermee kunt u de uiteindelijke afbeelding van de weergave splitsen in verschillende stroken of tegels, die afzonderlijk kunnen worden geleverd en naadloos kunnen worden samengevoegd door de client, zonder artefacten langs de randen.
solution: Experience Manager
title: rect
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1870001b-7904-470f-9582-984d453509ca
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 0%

---

# rect{#rect}

Eindweergaverechthoek. Hiermee kunt u de uiteindelijke afbeelding van de weergave splitsen in verschillende stroken of tegels, die afzonderlijk kunnen worden geleverd en naadloos kunnen worden samengevoegd door de client, zonder artefacten langs de randen.

`rect= *`coord`*, *`size`*[, *`schalen`*]`

<table id="simpletable_69D112F85FA24EFCA727B398DC8ED699"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p> </td> 
  <td class="stentry"> <p>Pixelverschuiving van de linkerbovenhoek van de weergaveafbeelding naar de linkerbovenhoek van de weergaverechthoek (int, int), uitgedrukt in pixels, na <span class="varname"> schalen</span> wordt toegepast. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> size</span> </p></td> 
  <td class="stentry"> <p>Grootte van de ROI in pixels (int, int). Hiermee geeft u de grootte van de antwoordafbeelding op. De afbeelding is gevuld met <span class="codeph"> bgc=</span> in gebieden die niet onder de afbeelding van de weergave vallen (of die transparant blijven, als <span class="codeph"> fmt=*-alpha</span> in het verzoek). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> schalen</span> </p></td> 
  <td class="stentry"> <p>Schaalfactor (reëel). Bij waarden kleiner dan 1,0 neemt de resolutie af en bij waarden groter dan 1,0 neemt de resolutie toe. </p></td> 
 </tr> 
</table>

Met deze opdracht kunnen via HTTP grote afbeeldingen worden geleverd die anders de maximale grootte overschrijden die is geconfigureerd met `attribute::MaxPix`.

>[!NOTE]
>
>Als u JPEG comprimeert, krijgt u het beste resultaat als de strip of tegelgrootte een veelvoud is van de tegelgrootte van de JPEG-codering (16 x 16 pixels).

## Voorbeeld {#section-932fcfcb41d74a29bc929e4430c49601}

Scheid een afdrukbare CMYK-afbeelding in verschillende strepen met volledige resolutie om de bestandsgrootte van het downloadbestand te beperken. Als wij om een aaneengesloten beeld zouden verzoeken:

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&fmt=tif&icc=WebCoated`

Eerst wordt relevante informatie over de afbeelding verkregen:

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&req=props`

De tekstreactie bevat de volgende eigenschappen:

`image.width=2000 image.height=2400 image.version=37JK6NTvpvC42F5gOuLEVY`

Op basis van deze informatie kiezen we voor vier stroken van 600 x 2000 pixels. De `rect=` wordt gebruikt om de stripgrootte en de posities te beschrijven.

Aangezien deze afbeelding regelmatig wordt gewijzigd, worden de `id=` gebruiken om de kans te minimaliseren dat wij omhoog met één of meerdere stroken van een oudere versie van het beeld eindigen die in een CDN of volmachtsserver in het voorgeheugen kunnen zijn opgeslagen. De waarde van de `image.version` eigenschap wordt voor dit doel gebruikt.

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,0,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,600,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1200,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1800,2000,600`

## Eigenschappen {#section-aae223cee13e46d38b74680c048d945b}

Kenmerk weergeven. Is van toepassing ongeacht de huidige laaginstelling.

Om het even welke gebieden van het ROI die zich buiten het meningsbeeld uitbreiden worden opgevuld met `bgc=`.

Belangrijk `rect=` is toegepast *na* definitieve schaling en aanpassing met `scl=`, `wid=`, `hei=`, `fit=`, `rgn=`, en `align=`.

## Standaard {#section-b296d3bbfb19441f87137a452b70f19a}

Gehele, ongewijzigde weergave-afbeelding ( `rect=0,0,width,height,1.0`).

## Zie ook {#section-74015202c0c545ec82aec614d74b4bbd}

[uitsnijden=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47), [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f), [kenmerk::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5), [id=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0)
