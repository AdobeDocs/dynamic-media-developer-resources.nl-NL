---
description: Genereert miniatuurafbeelding voor uw video.
seo-description: Genereert miniatuurafbeelding voor uw video.
seo-title: MediaOptions
solution: Experience Manager
title: MediaOptions
topic: Scene7 Image Production System API
uuid: 4de59678-1bef-484c-9a43-ded531537aeb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 0%

---


# MediaOptions{#mediaoptions}

Genereert miniatuurafbeelding voor uw video.

Syntaxis

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Naam </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoEncodingPresetsArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:HandleArray</span> </td> 
   <td colname="col3">Een array met <span class="codeph"> PropertySet</span> handvatten die verwijzen naar videocoderingsvoorinstellingen voor het transcoderen van video's. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> generateThumbnail</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3"> Indien waar (true), wordt het eerste frame van de video geëxtraheerd en gebruikt als miniatuurafbeelding. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> miniatuurOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typen:ThumbnailOptions</span> </td> 
   <td colname="col3">Optioneel. Hiermee kunt u een bepaald videoframe kiezen dat u als miniatuurafbeelding wilt gebruiken. <p>Als u een miniatuurafbeelding wilt opgeven, geeft u de tijd (in milliseconden vanaf het begin van de video) door voor het frame dat u wilt gebruiken. Waarden kunnen variëren van 0 tot het einde van de video. <p>Opmerking: Als u de tijd onjuist opgeeft, wordt <span class="codeph"> generateThumbnail</span> standaard ingesteld op true. </p></p><p>Zie <a href="../../types/c-data-types/r-thumbnail-options.md#reference-370088b0a4ce4096b9b3e5489a368b5c" format="dita" scope="local"> ThumbnailOptions</a>. </p></td> 
  </tr> 
 </tbody> 
</table>

## Voorbeeld {#section-a9356de782d74af6933c39fa7ad12212}

```
<complexType name="MediaOptions">
        <sequence>
            <element name="videoEncodingPresetsArray" type="types:HandleArray" minOccurs="0"/>
            <element name="generateThumbnail" type="xsd:boolean" minOccurs="0"/>
            <element name="thumbnailOptions" type="types:ThumbnailOptions" minOccurs="0"/>
        </sequence>
    </complexType>
```

## Wordt gebruikt door {#section-87cb83407198432c95eaa2db9f12f9db}

Het type `mediaOptions` wordt gebruikt door:

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadURLsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)

