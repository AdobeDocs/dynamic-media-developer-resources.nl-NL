---
description: Weergavehoogte. Hiermee geeft u de hoogte van de antwoordafbeelding op.
seo-description: Weergavehoogte. Hiermee geeft u de hoogte van de antwoordafbeelding op.
seo-title: hei
solution: Experience Manager
title: hei
topic: Scene7 Image Serving - Image Rendering API
uuid: 6f7e580b-6399-4661-b5d9-8044574ba124
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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

Rasterindelingen worden gerenderd met de instelling Standaardweergavegrootte (of Standaardpixel). Klik op **[!UICONTROL Application Setup]** > **[!UICONTROL Publish Setup]** > **[!UICONTROL Image Server]** en voer vervolgens de waarden voor Breedte en Hoogte in. Kleinere formaten bieden betere prestaties. U moet uw instellingen opslaan en een afbeelding publiceren om een wijziging toe te passen.

Als u een `scale=1` opdracht toepast, wordt een verzoek voor een rasterindeling gerenderd met de grootte die in de FXG is opgegeven.

## Standaard {#section-76ee3daa77cb468ab310821357cc9404}

Als noch `wid=`, `hei=`noch `scale=` worden gespecificeerd, is het antwoordbeeld de standaardmeningsgrootte die in het FXG- dossier wordt gespecificeerd.

## Voorbeeld {#section-a91c14d31e71481ba054412d9f642885}

[!DNL http://server/is/agm/myRootId/myImageId?hei=200]

Tenzij een indeling is opgegeven, wordt de afbeelding weergegeven als een SWF-bestand. In dit geval hebben hoogte en breedte geen betekenis, omdat het SWF-bestand gewoonlijk wordt uitgebreid tot de grootte van het browservenster. Dit heeft tot gevolg dat dit en het woord alleen van toepassing zijn op raster- of PDF-indelingen. Voorbeelden van rasterindelingen zijn:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alfa
* TIF-alfa
* PNG-alfa

