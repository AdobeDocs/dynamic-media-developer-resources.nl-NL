---
title: UnCompressOptions
description: Instelling voor uploaden om ZIP- en TAR-bestanden te verwerken als primaire elementen (Geen) of om de inhoud ervan te extraheren en te uploaden (UnCompress).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 89222959-3701-4ea6-bcae-98ceec93764f
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---

# [!DNL UnCompressOptions]{#uncompressoptions}

Instelling voor uploaden om ZIP- en TAR-bestanden te verwerken als primaire elementen (Geen) of om de inhoud ervan te extraheren en te uploaden (UnCompress).

>[!NOTE]
>
>De instelling `None` is de standaardwaarde.

## Parameters {#section-10e49e27f60743da970a4ff1c4587eab}

<table id="table_89C2F7CDB24848459E47F1F7F58D91BA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Naam </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> proces</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> <p>Bepaalt de verwerking van ZIP- en TAR-archiefbestanden. Deze biedt twee opties: 
     <ul id="ul_F34E2F3B9B74450CA7E76BD9FD7137C2">
      <li id="li_E982468ED814446593B0C0A3F3D729FB"><span class="codeph"> Geen:</span> Verwerk het als primaire elementen. </li>
      <li id="li_4A45DA99592B4EF7A1FE0A946A835104"><span class="codeph"> Comprimeren ongedaan maken:</span> Extraheer en verwerk de inhoud. </li>
     </ul><p>Opmerking: tekenreeksconstanten zijn hoofdlettergevoelig. Gebruiken <span class="codeph"> UnCompress</span>, niet <span class="codeph"> decomprimeren</span>, of <span class="codeph"> unCompress</span>. </p></p> </td> 
  </tr> 
 </tbody> 
</table>

## Voorbeeld {#section-48fd14af768a436284c31692038579a8}

```
 <!-- uncompress zip/tar/gzip files -->
            <element name="unCompressOptions" type="types:UnCompressOptions" minOccurs="0"/>
    <complexType name="UnCompressOptions">
        <sequence>
            <!-- Options: None (default),UnCompress -->
            <element name="process" type="xsd:string"/>
        </sequence>
    </complexType>
```

## Gebruikt door {#section-b2a829cf5511412e968bb2000f85cc31}

De `unCompressionOptions` type wordt gebruikt door:

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)
