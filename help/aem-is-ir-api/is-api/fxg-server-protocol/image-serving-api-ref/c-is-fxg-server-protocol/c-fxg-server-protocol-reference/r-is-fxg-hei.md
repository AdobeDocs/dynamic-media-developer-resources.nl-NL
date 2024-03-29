---
title: hei
description: Weergavehoogte. Hiermee geeft u de hoogte van de antwoordafbeelding op.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dcc9311d-4157-490b-9fc4-47060ddb0e37
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---

# hei{#hei}

Weergavehoogte. Hiermee geeft u de hoogte van de antwoordafbeelding op.

`hei= *`val`*`

<table id="simpletable_627E67D201744588815325F3C55F76A5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Hoogte van afbeelding in pixels (int groter dan 0). </p></td> 
 </tr> 
</table>

Rasterindelingen worden weergegeven met de instelling Standaardweergavegrootte (of Standaardpixel). Selecteren **[!UICONTROL Application Setup]** > **[!UICONTROL Publish Setup]** > **[!UICONTROL Image Server]** Voer vervolgens de waarden voor Breedte en Hoogte in. Kleinere formaten bieden betere prestaties. Sla uw instellingen op en voer een publicatie met afbeeldingsgegevens uit om een wijziging toe te passen.

Als u een `scale=1` een rasterindelingsverzoek wordt weergegeven met de grootte die in de FXG is opgegeven.

## Standaard {#section-76ee3daa77cb468ab310821357cc9404}

Indien `wid=`, `hei=`, of `scale=` niet zijn opgegeven, is de antwoordafbeelding de standaardweergavegrootte die in het FXG-bestand is opgegeven.

## Voorbeeld {#section-a91c14d31e71481ba054412d9f642885}

[!DNL `http://server/is/agm/myRootId/myImageId?hei=200`]

Tenzij een indeling is opgegeven, wordt de afbeelding weergegeven als een SWF-bestand. In dit geval hebben hoogte en breedte geen betekenis, omdat de SWF gewoonlijk wordt vergroot tot de grootte van het browservenster. Hierdoor zijn hei en wid alleen van toepassing op raster- of PDF-indelingen. Voorbeelden van rasterindelingen zijn:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* TIF-alfa
* PNG-alfa
