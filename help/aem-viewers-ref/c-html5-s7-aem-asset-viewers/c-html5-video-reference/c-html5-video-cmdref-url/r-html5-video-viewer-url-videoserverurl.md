---
description: URL-opdracht voor video-viewer.
solution: Experience Manager
title: videoServerUrl
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 945c32e0-a67b-4c27-b661-26510615d757
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 1%

---

# videoServerUrl{#videoserverurl}

URL-opdracht voor video-viewer.

` videoServerUrl= *`videoRootPath`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> videoRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p> Het hoofdpad van de videoserver. Als geen domein wordt gespecificeerd, dan wordt het domein waarvan de pagina wordt gediend toegepast in plaats daarvan. De standaardresolutie voor URI-paden is van toepassing. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-f42369774e2740dcb399626a0e4e930e}

Optioneel. Niet nodig voor standaard SaaS-gebruik.

## Standaard {#section-d016470e92a74f98a18c4ab3489410a5}

`/is/content/`

## Voorbeeld {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
videoServerUrl=http://s7d1.scene7.com/is/content/
```
