---
title: VideoPlayer.ssl
description: Configuration attribute for Interactive Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 16e17e2f-be98-4a5a-ba5e-5d18e7f76fa4
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# VideoPlayer.ssl{#videoplayer-ssl}

Configuration attribute for Interactive Video Viewer.

<!-- >[!NOTE]
>
>This configuration attribute only applies to AEM 6.2 with installation of [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

`[VideoPlayer.|<containerId>_videoPlayer.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|on</span> </p> </td> 
   <td colname="col2"> <p> Bepaalt of de video wordt geleverd via een HTTPS (Secure SSL Connection) of een onveilige verbinding (HTTP). </p> <p>Wanneer ingesteld op <span class="codeph"> auto</span> het protocol voor de levering van video wordt overgenomen van het protocol van de ingebedde webpagina. Als de webpagina via HTTPS wordt geladen, wordt de video ook via HTTPS geleverd en omgekeerd. Wanneer de webpagina zich op HTTP bevindt, wordt de video via HTTP geleverd. </p> <p>Wanneer ingesteld op <span class="codeph"> op</span>De video wordt altijd geleverd via een beveiligde verbinding, ongeacht het protocol van de webpagina. </p> <p>Heeft alleen invloed op gepubliceerde video-oplevering en wordt genegeerd voor videovoorvertoning in de modus Auteur. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-f42369774e2740dcb399626a0e4e930e}

Optioneel.

## Standaard {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## Voorbeeld {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
ssl=on
```

<!--<a id="section_5943AC73316749C68761FF7F74DA7547"></a>-->

Zie ook [Beveiligde video-levering](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-securevideodelivery.md#concept-13f66fdd4a52494aa516cd0f36fdac27).
