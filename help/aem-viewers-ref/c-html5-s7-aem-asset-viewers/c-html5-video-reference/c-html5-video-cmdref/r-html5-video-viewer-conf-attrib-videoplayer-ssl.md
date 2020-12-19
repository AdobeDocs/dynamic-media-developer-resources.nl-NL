---
description: Configuration attribute for Video Viewer.
seo-description: Configuration attribute for Video Viewer.
seo-title: VideoPlayer.ssl
solution: Experience Manager
title: VideoPlayer.ssl
topic: Dynamic media
uuid: 969da9ea-c97c-4fa8-9207-21d6302609e5
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---


# VideoPlayer.ssl{#videoplayer-ssl}

Configuration attribute for Video Viewer.

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

Zie ook [Beveiligde videoverstrekking](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-securevideodelivery.md#concept-cf9d1346a07d4429b0c6c32c9cac50ff).
