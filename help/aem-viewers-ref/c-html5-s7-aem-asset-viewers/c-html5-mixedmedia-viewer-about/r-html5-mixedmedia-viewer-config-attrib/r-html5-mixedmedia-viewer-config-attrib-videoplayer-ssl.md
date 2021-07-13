---
description: Configuration attribute for Mixed Media Video Viewer.
solution: Experience Manager
title: VideoPlayer.ssl
feature: Dynamic Media Classic,Viewers,SDK/API,Gemengde mediasets
role: Developer,User
exl-id: 5fd3aa39-edb0-4434-aa5f-e511c84cf950
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# VideoPlayer.ssl{#videoplayer-ssl}

Configuration attribute for Mixed Media Video Viewer.

>[!NOTE]
>
>Dit configuratiekenmerk is alleen van toepassing op AEM 6.2 met installatie van [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) en op AEM 6.1 met installatie van [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

`[VideoPlayer.|<containerId>_videoPlayer.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|on</span> </p> </td> 
   <td colname="col2"> <p> Bepaalt of de video wordt geleverd via een HTTPS (Secure SSL Connection) of een onveilige verbinding (HTTP). </p> <p>Wanneer ingesteld op <span class="codeph"> auto</span>, wordt het protocol voor het leveren van de video overgenomen van het protocol van de ingesloten webpagina. Als de webpagina via HTTPS wordt geladen, wordt de video ook via HTTPS geleverd en andersom. Wanneer de webpagina zich op HTTP bevindt, wordt de video via HTTP geleverd. </p> <p>Wanneer ingesteld op <span class="codeph"> op</span>, vindt de levering van de video altijd plaats over een veilige verbinding ongeacht het protocol van de Web-pagina. </p> <p>Heeft alleen invloed op gepubliceerde video-oplevering en wordt genegeerd voor videovoorvertoning in de modus Auteur. </p> </td> 
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

Zie ook [Beveiligde videoverstrekking](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-securevideodelivery.md#concept-4d155111df9f469aa6c6d7b41e959dcb).
