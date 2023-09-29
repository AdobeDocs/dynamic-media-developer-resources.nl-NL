---
title: winderig
description: Weergavebreedte. Hiermee geeft u de breedte van de antwoordafbeelding (weergaveafbeelding) op.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5edd045c-600e-4295-9672-04a5c3bc651d
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '166'
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

Als geen van beide `wid=`, `hei=`, noch `scale=` opgegeven, is de antwoordafbeelding de standaardweergavegrootte die in het FXG-bestand is opgegeven.

Rasterindelingen worden weergegeven met de instelling Standaardweergavegrootte (of Standaardpixel). Klikken **[!UICONTROL Application Setup]** > **[!UICONTROL Publish Setup]** > **[!UICONTROL Image Server]** Voer vervolgens de waarden voor Breedte en Hoogte in. Kleinere formaten bieden betere prestaties. Sla uw instellingen op en voer een publicatie met afbeeldingsgegevens uit om een wijziging toe te passen.

Als u een `scale=1` een rasterindelingsverzoek wordt weergegeven met de grootte die in de FXG is opgegeven.

## Voorbeeld {#section-2f72cb2653d54c6aaacf0d97521fb72c}

`http://server/is/agm/myRootId/myImageId?wid=200`

Tenzij een indeling is opgegeven, wordt de afbeelding weergegeven als een SWF-bestand. In dit geval hebben hoogte en breedte geen betekenis, omdat de SWF gewoonlijk wordt vergroot tot de grootte van het browservenster. Dientengevolge, `hei` en `wid` alleen van toepassing op raster- of PDF-indelingen. Voorbeelden van rasterindelingen zijn:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* TIF-alfa
* PNG-alfa
