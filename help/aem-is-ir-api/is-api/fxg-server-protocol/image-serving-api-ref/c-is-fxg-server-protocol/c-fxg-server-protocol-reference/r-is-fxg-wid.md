---
description: Weergavebreedte. Hiermee geeft u de breedte van de antwoordafbeelding (weergaveafbeelding) op.
solution: Experience Manager
title: winderig
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 5edd045c-600e-4295-9672-04a5c3bc651d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 0%

---

# winderig{#wid}

Weergavebreedte. Hiermee geeft u de breedte van de antwoordafbeelding (weergaveafbeelding) op.

`wid= *`val`*`

<table id="simpletable_8229FEFB366F4A799C206FD3E3C601BA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Afbeeldingsbreedte in pixels (int groter dan 0), </p></td> 
 </tr> 
</table>

## Standaard {#section-830bae0b6bac440098444d7cdcb23e2e}

Als noch `wid=`, `hei=`, noch `scale=` worden gespecificeerd, is het antwoordbeeld de standaardmeningsgrootte die in het FXG- dossier wordt gespecificeerd.

Rasterindelingen worden gerenderd met de instelling Standaardweergavegrootte (of Standaardpixel). Klik **[!UICONTROL Application Setup]** > **[!UICONTROL Publish Setup]** > **[!UICONTROL Image Server]**, dan ga uw waarden van de Breedte en van de Hoogte in. Kleinere formaten bieden betere prestaties. U moet uw instellingen opslaan en een afbeelding publiceren om een wijziging toe te passen.

Als u een `scale=1` bevel toepast, wordt een rasterformaatverzoek teruggegeven bij de grootte die in FXG wordt gespecificeerd.

## Voorbeeld {#section-2f72cb2653d54c6aaacf0d97521fb72c}

[!DNL http://server/is/agm/myRootId/myImageId?wid=200]

Tenzij een indeling is opgegeven, wordt de afbeelding weergegeven als een SWF-bestand. In dit geval hebben hoogte en breedte geen betekenis, omdat het SWF-bestand gewoonlijk wordt uitgebreid tot de grootte van het browservenster. Dit heeft tot gevolg dat dit en het woord alleen van toepassing zijn op raster- of PDF-indelingen. Voorbeelden van rasterindelingen zijn:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alfa
* TIF-alfa
* PNG-alfa
