---
title: KnockoutBackgroundOptions
description: Hiermee maskeert u de achtergrond voor geselecteerde afbeeldingen (neemt u af). Met dit gegevenstype kunt u de lagen in andere lagen bedekken met transparantie buiten de afbeelding van het onderwerp. Een optionele parameter die standaard uitgeschakeld is.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: aed8cf2e-5a09-43ff-9420-0d0d54059515
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 0%

---

# [!DNL KnockoutBackgroundOptions]{#knockoutbackgroundoptions}

Hiermee maskeert u de achtergrond voor geselecteerde afbeeldingen (neemt u af). Met dit gegevenstype kunt u de lagen in andere lagen bedekken met transparantie buiten de afbeelding van het onderwerp.

Dit gegevenstype is standaard optioneel en uitgeschakeld.

`KnockoutBackgroundOptions=[corner, tolerance, fill]`

## Parameters {#section-3149b49ccb714e6eafa6655354816819}

>[!IMPORTANT]
>
>Als u configureert `KnockoutBackgroundOptions` in Adobe Experience Manager, gebruik in plaats daarvan de volgende parameters:
>* `kbCorner`
>* `kbTolerance`
>* `kbFillMethod`
>
>Bijvoorbeeld: `kbCorner=UpperLeft&kbTolerance=0.2&kbFillMethod=MatchPixel`

<table id="table_68131DE0A3C84908A43C6F7777F20973"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Naam </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> hoek</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3">Hiermee selecteert u de hoek waarmee u wilt werken. <span class="codeph"> hoek</span> Accepteert deze waarden: 
    <ul id="ul_36C2F07706764A7081010D5521BF3096">
     <li id="li_CBACE5C6AA8C48D3BEE033D3AE03AF3C"><span class="codeph"> BovenkantLinks</span></li>
     <li id="li_49AC53536B4B4D2CA3DD89E2A2B2E95D"><span class="codeph"> BottomLeft</span></li>
     <li id="li_7AD372FF4A9B48F0A16964EE9CB3EE88"><span class="codeph"> UpperRight</span></li>
     <li id="li_D31476DD9A8E4BDBB13A6DDA46547877"><span class="codeph"> BottomRight</span></li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tolerantie</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dubbel</span> </td> 
   <td colname="col3">Een optionele instelling die witruimte verwijdert van afbeeldingsranden op basis van transparantie. Accepteert een reeks waarden van 0,0 tot en met 1,0. Opgeven: 
    <ul id="ul_FE5423B857AE43FCBA7A9AEA76C754CC">
     <li id="li_01E3BD0AB8DA4C408B47CB02B269404A">0 om de kleuren exact overeen te laten komen. </li>
     <li id="li_FCE21384265D4ECE9C0D785F1BB32C3A">1 om de meeste kleurverschillen mogelijk te maken. </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fillMethod</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> <p>Pixeltransparantie bepalen op de locatie die wordt opgegeven door het dialoogvenster <span class="codeph"><span class="varname"> hoek</span></span> variabele. De <span class="codeph"> fillMethod</span> Accepteert deze waarden: </p> 
    <ul id="ul_D95F3B613D344BB89487ED09D83F9217"> 
     <li id="li_3D7B7CA1B9094D16A98E0BA3D962E97F"> <span class="codeph"> FloodFill</span>: Hiermee worden alle pixels in de opgegeven hoek transparant gemaakt. </li> 
     <li id="li_F97343C3DA7644BCBD1748AD8F9DCE2E"> <span class="codeph"> MatchPixel</span>: Hiermee worden alle overeenkomende pixels transparant gemaakt, ongeacht de locatie. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Voorbeeld {#section-3f9edfff321a4e4394f766298b9e284d}

```
<complexType name="KnockoutBackgroundOptions">
        <sequence>
            <!-- corner one of UpperLeft, BottomLeft, UpperRight, BottomRight -->
            <element name="corner" type="xsd:string" minOccurs="1"/>
            <!-- Tolerance real value between 0.0 and 1.0 -->
            <element name="tolerance" type="xsd:double" minOccurs="0"/>
            <!-- one of FloodFill or MatchPixel is required -->
            <element name="fillMethod" type="xsd:string" minOccurs="1"/>
        </sequence>
    </complexType>
```

## Gebruikt door {#section-28c43baafe85434a9ee9e303ed10569a}

De `KnockoutBackgroundOptions` type wordt gebruikt door:

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)
