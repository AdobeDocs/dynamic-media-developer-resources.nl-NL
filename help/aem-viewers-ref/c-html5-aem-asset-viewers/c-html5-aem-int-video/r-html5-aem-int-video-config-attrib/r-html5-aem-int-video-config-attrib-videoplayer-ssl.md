---
description: Configuration attribute for Interactive Video Viewer.
seo-description: Configuration attribute for Interactive Video Viewer.
seo-title: VideoPlayer.ssl
solution: Experience Manager
title: VideoPlayer.ssl
topic: Dynamic media
uuid: b4929e14-8712-4923-b9b1-62aa6721fc99
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# VideoPlayer.ssl{#videoplayer-ssl}

Configuration attribute for Interactive Video Viewer.

>[!NOTE]
>
>Dit configuratiekenmerk is alleen van toepassing op AEM 6.2 met installatie van [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) en op AEM 6.1 met installatie van [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

`[VideoPlayer.|<containerId>_videoPlayer.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|on</span> </p> </td> 
   <td colname="col2"> <p> Bepaalt of de video wordt geleverd via een HTTPS (Secure SSL Connection) of een onveilige verbinding (HTTP). </p> <p>Wanneer deze optie is ingesteld op <span class="codeph"> auto</span> , wordt het protocol voor het leveren van video overgenomen van het protocol van de ingesloten webpagina. Als de webpagina via HTTPS wordt geladen, wordt de video ook via HTTPS geleverd en andersom. Wanneer de webpagina zich op HTTP bevindt, wordt de video via HTTP geleverd. </p> <p>Wanneer ingesteld op <span class="codeph"> on</span>, vindt de levering van video altijd plaats via een beveiligde verbinding, ongeacht het protocol van de webpagina. </p> <p>Heeft alleen invloed op gepubliceerde video-oplevering en wordt genegeerd voor videovoorvertoning in de modus Auteur. </p> </td> 
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
