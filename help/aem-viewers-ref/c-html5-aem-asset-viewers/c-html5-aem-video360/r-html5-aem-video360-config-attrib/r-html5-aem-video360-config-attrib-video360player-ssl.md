---
title: Video360Player.ssl
description: Configuration attribute for Video360 Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 44efa378-c911-4449-8a10-61212d4392c6
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 3%

---

# Video360Player.ssl{#video-player-ssl}

Configuration attribute for Video360 Viewer.

<!-- >[!NOTE]
>
>This configuration attribute only applies to AEM 6.2 with installation of [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

`[Video360Player.|<containerId>_video360Player.]ssl=auto|on`

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

Zie ook [Beveiligde video-levering](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-securevideodelivery.md#concept-13f66fdd4a52494aa516cd0f36fdac27).
