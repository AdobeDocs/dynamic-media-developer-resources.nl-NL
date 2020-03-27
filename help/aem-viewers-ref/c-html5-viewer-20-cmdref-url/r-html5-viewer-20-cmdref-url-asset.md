---
description: Parameter die alle viewers gemeen hebben.
seo-description: Parameter die alle viewers gemeen hebben.
seo-title: element
solution: Experience Manager
title: element
topic: Dynamic media
uuid: 6a72257f-d204-4258-b6f8-de6f7b00fd54
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# asset{#asset}

Parameter die alle viewers gemeen hebben.

` asset= *`assetId`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> element-id </span></span> </p> </td> 
   <td colname="col2"> <p> De element-id van de enkele video of Adaptieve videoset. </p> </td> 
  </tr> 
 </tbody> 
</table>

Deze eigenschap is vereist, tenzij `video` parameter wordt gebruikt. Zie [External Video Support](../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3) under Video or [External video support](../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760) under Video360.

of

` asset= *`image`*`

<table id="table_67E18F42E97C4AAAB0A2F67B7924765D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> afbeelding </span></span> </p> </td> 
   <td colname="col2"> <p> Hiermee geeft u één afbeelding of carrouselset op. Dubbele HTTP-codering toepassen op elk onveilig teken in de naam van de afbeelding of de carrouselset. </p> </td> 
  </tr> 
 </tbody> 
</table>

of

` asset= *``* | *``* | *``* | *``* [%3F *`imageimageListImageListWithModihermultiDimensionalSpinSetmodifiers`*]`

<table id="table_A2A0ACD942E942BC99AF0DC80FB1C670"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> afbeelding </span></span> </p> </td> 
   <td colname="col2"> <p> Hiermee geeft u één afbeelding op. Dubbele HTTP-codering toepassen op elk onveilig teken in de afbeeldingsnaam. </p> <p>Of geeft een verwijzing naar een afbeeldingsset op. De kijker wint beeldreeksen van de server terug, gebruikend req=set IS <span class="codeph"> </span> verzoek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> afbeeldingslijst </span></span> </p> </td> 
   <td colname="col2"> <p> Hiermee geeft u een expliciete afbeeldingsset op, bestaande uit een gesorteerde reeks items of frames, gescheiden door komma's. </p> <p> <p>Opmerking:  Deze eigenschap wordt gesteund in het Publiceren van Adobe Scene7 Systeem; wordt niet ondersteund in Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> imageListWithModifiers </span></span> </p> </td> 
   <td colname="col2"> <p> Hiermee geeft u een expliciete afbeeldingsset op waarin elk frame zijn eigen wijzigingstoetsen voor afbeeldingsservers heeft. In dit geval wordt de lijst met kaders tussen haakjes geplaatst. Zorg ervoor dat u dubbele HTTP-codering toepast op elke komma die aanwezig is in de frame-specifieke Image Serving-modifier. </p> <p> <p>Opmerking:  Deze eigenschap wordt gesteund in het Publiceren van Adobe Scene7 Systeem; wordt niet ondersteund in Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> multiDimensionalSpinSet </span></span> </p> </td> 
   <td colname="col2"> <p>Hiermee wordt een expliciete multidimensionale spin-set opgegeven met de volgende syntaxis: </p> <p> <span class="codeph"> (( <span class="varname"> horizontalSpinSet </span>)[,( <span class="varname"> horizontalSpinSet </span>)] </span> </p> <p> waarbij <span class="codeph"> horizontalSpinSet <span class="varname"> een door komma's gescheiden lijst met frames </span> </span> is voor een bepaalde horizontale as. Alle <span class="codeph"> horizontaleSpinSet <span class="varname"> </span> </span> moet hetzelfde aantal frames hebben. </p> <p> <p>Opmerking:  Deze eigenschap wordt gesteund in het Publiceren van Adobe Scene7 Systeem; wordt niet ondersteund in Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> modifiers </span></span> </p> </td> 
   <td colname="col2"> <p> Opdrachten Beeldservers; <span class="codeph"> &amp; </span> and <span class="codeph"> = </span> separators moeten HTTP-gecodeerd zijn als <span class="codeph"> %26 </span> en <span class="codeph"> %3D </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

of

` asset=( *``* | ( *``*; *``* | *``*; *``* | *``*; *``*); *``*;( *``*; *``* | *``*; *``* | *``*; *``*); *``*;] [%3F *`mediaSetvideoswatchIdimageswatchIdsetIdswatchIdIDvideoswatchIdimageswatchIdsetIdswatchIdIDmodifiers`*]`

<table id="table_D31C8507C02A4452A79DEDDEC62EF2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Mediaset </span></span> </p> </td> 
   <td colname="col2"> <p> Hiermee wordt een verwijzing naar een mediaset opgegeven. De viewer haalt mediasets van de server op met behulp van de aanvraag req=set IS. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> video </span></span> </p> </td> 
   <td colname="col2"> <p> Eén video of Adaptieve videoset. </p> <p> <p>Opmerking:  Deze eigenschap wordt gesteund in het Publiceren van Adobe Scene7 Systeem; wordt niet ondersteund in Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> afbeelding </span></span> </p> </td> 
   <td colname="col2"> <p> Eén afbeelding. </p> <p> <p>Opmerking:  Deze eigenschap wordt gesteund in het Publiceren van Adobe Scene7 Systeem; wordt niet ondersteund in Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> setId </span></span> </p> </td> 
   <td colname="col2"> <p> Staalset. </p> <p> <p>Opmerking:  Deze eigenschap wordt gesteund in het Publiceren van Adobe Scene7 Systeem; wordt niet ondersteund in Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> staal-id </span></span> </p> </td> 
   <td colname="col2"> <p>Staalafbeelding. </p> <p> <p>Opmerking:  Deze eigenschap wordt gesteund in het Publiceren van Adobe Scene7 Systeem; wordt niet ondersteund in Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ID </span></span> </p> </td> 
   <td colname="col2"> <p> De het punttype herkenningsteken van de Plaats van media kan één van het volgende zijn: </p> <p> 
     <ul id="ul_3100F9356628498DA820C07F6F69CC9B"> 
      <li id="li_51B649A539F14510873CFDA85A6AA714"> <p> <span class="codeph"> advanced_image </span> </p> <p>Voor één afbeelding. </p> </li> 
      <li id="li_7E764D67294647C1A828F949E5ED1908"> <p> <span class="codeph"> advanced_swatchset </span> </p> <p>Voor geneste stalenset. </p> </li> 
      <li id="li_C942CED779B54110BCDC74188995FD5B"> <p> <span class="codeph"> draaien </span> </p> <p>Voor centrifugeerset. </p> </li> 
      <li id="li_6EA5C54F078D4B24B44F1588BF083842"> <p> <span class="codeph"> video </span> </p> <p>Voor één video. </p> </li> 
      <li id="li_8110FA7E0CAB4681A2D8C15F2A656E69"> <p> <span class="codeph"> video_set </span> </p> <p>Voor adaptieve videosets. </p> </li> 
     </ul> </p> <p> <p>Opmerking:  Deze eigenschap wordt gesteund in het Publiceren van Adobe Scene7 Systeem; wordt niet ondersteund in Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> modifiers </span></span> </p> </td> 
   <td colname="col2"> <p> Opdrachten Beeldservers; <span class="codeph"> &amp; </span> and <span class="codeph"> = </span> separators moeten HTTP-gecodeerd zijn als <span class="codeph"> %26 </span> en <span class="codeph"> %3D </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Afbeeldingen die gebruikmaken van IR (Image Rendering) of UGC (Door de gebruiker gegenereerde inhoud) worden niet ondersteund door deze viewer.

## Eigenschappen {#section-10ee45d637134e0fbcd943c62578cb78}

Vereist.

## Standaard {#section-d411e450028c460392cb8508f8ccc5d9}

Geen.

## Voorbeelden {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

Verwijzing naar enkel element:

```
asset=Scene7SharedAssets/Backpack_B
```

of

```
asset=/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg
```

of

```
asset=/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4
```

of

```
asset=/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner
```

of

```
asset=Viewers/space_station_360-AVS
```

Eén verwijzing naar een afbeeldingsset die is gedefinieerd in een catalogus:

```
asset=Viewers/Pluralist
```

Expliciete afbeeldingsset:

```
asset=Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C
```

Expliciete afbeelding ingesteld met frame-specifieke opties voor afbeeldingsservers:

```
asset=(Scene7SharedAssets/Backpack_B%3Fop_colorize%3D255%252C0%252C0,Scene7SharedAssets/Backpack_B%3Fop_colorize%3D0x00ff00)
```

Eén verwijzing naar een centrifugeset die is gedefinieerd in een catalogus:

```
asset=Scene7SharedAssets/SpinSet-Sample
```

Expliciete centrifugeerset:

```
asset=Scene7SharedAssets/Frame-1,Scene7SharedAssets/Frame-2,Scene7SharedAssets/Frame-3,Scene7SharedAssets/Frame-4,Scene7SharedAssets/Frame-5,Scene7SharedAssets/Frame-6,Scene7SharedAssets/Frame-7,Scene7SharedAssets/Frame-8
```

Expliciete multidimensionale centrifuge:

```
asset=((Scene7SharedAssets/ring1-25,Scene7SharedAssets/ring1-26,Scene7SharedAssets/ring1-27,Scene7SharedAssets/ring1-28,Scene7SharedAssets/ring1-29,Scene7SharedAssets/ring1-30,Scene7SharedAssets/ring1-31,Scene7SharedAssets/ring1-32,Scene7SharedAssets/ring1-33,Scene7SharedAssets/ring1-34,Scene7SharedAssets/ring1-35,Scene7SharedAssets/ring1-36),(Scene7SharedAssets/ring1-13,Scene7SharedAssets/ring1-14,Scene7SharedAssets/ring1-15,Scene7SharedAssets/ring1-16,Scene7SharedAssets/ring1-17,Scene7SharedAssets/ring1-18,Scene7SharedAssets/ring1-19,Scene7SharedAssets/ring1-20,Scene7SharedAssets/ring1-21,Scene7SharedAssets/ring1-22,Scene7SharedAssets/ring1-23,Scene7SharedAssets/ring1-24),(Scene7SharedAssets/ring1-01,Scene7SharedAssets/ring1-02,Scene7SharedAssets/ring1-03,Scene7SharedAssets/ring1-04,Scene7SharedAssets/ring1-05,Scene7SharedAssets/ring1-06,Scene7SharedAssets/ring1-07,Scene7SharedAssets/ring1-08,Scene7SharedAssets/ring1-09,Scene7SharedAssets/ring1-10,Scene7SharedAssets/ring1-11,Scene7SharedAssets/ring1-12))
```

Verwijzing naar enkele gemengde mediaset:

```
 asset=Scene7SharedAssets/Mixed_Media_Set_Sample
```

Expliciet gemengde mediaset:

```
asset=Scene7SharedAssets/Backpack_J;;advanced_image;,Scene7SharedAssets/Frame-6;;advanced_image;,Scene7SharedAssets/Frame-2;;advanced_image;,Scene7SharedAssets/SpinSet_Sample;;spin;,Scene7SharedAssets/ImageSet-Colors-Sample;;advanced_swatchset;,Scene7SharedAssets/Glacier_Climber_640x360;Scene7SharedAssets/Glacier_Climber_640x360;video;
```

De optie Verscherpen is toegevoegd aan alle afbeeldingen in de set:

```
asset=Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C%3Fop_sharpen=%3D1
```

```
asset=Scene7SharedAssets/Mixed_Media_Set_Sample%3Fop_sharpen%3D1
```

```
asset=Viewers/Pluralist%3Fop_sharpen%3D1
```

