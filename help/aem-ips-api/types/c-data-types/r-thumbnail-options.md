---
description: Een optioneel type waarmee u een bepaald videoframe kunt kiezen dat u als miniatuurafbeelding wilt gebruiken.
solution: Experience Manager
title: ThumbnailOptions
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 7d84590d-2227-4d9a-9cb0-0f4b1fcabd8e
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---

# ThumbnailOptions{#thumbnailoptions}

Een optioneel type waarmee u een bepaald videoframe kunt kiezen dat u als miniatuurafbeelding wilt gebruiken.

Syntaxis

## Parameters {#section-b1777bf868764a7099d4a954b471856c}

<table id="table_C71FD0C995D94CE18994CDA2DC3460DF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Naam </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> miniatuurTime</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> <p>Hiermee stelt u de tijd (in milliseconden vanaf het begin van de video) in voor het frame dat u wilt gebruiken voor de videominiatuur. Waarden kunnen variëren van 0 tot het einde van de video. <p>Opmerking: Het systeem gebruikt het eerste frame van de video voor de miniatuur als u de tijd onjuist opgeeft. Zie <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </p></p> </td> 
  </tr> 
 </tbody> 
</table>

## Voorbeeld {#section-ce3b59c60fea4cd4945427a025051447}

```
<complexType name="ThumbnailOptions">
     <sequence>
        <element name="thumbnailTime" type="xsd:long" minOccurs="0"/>
      </sequence>
</complexType>
```
