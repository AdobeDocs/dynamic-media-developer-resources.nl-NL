---
title: HTTPS-video leveren
description: HTTPS-video leveren
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: f9651405-ebc6-4b1f-8fb6-031d0b295083
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---

# HTTPS-video leveren{#https-video-delivery}

<!-- >[!NOTE]
>
>Secure Video Delivery only applies to AEM 6.2 with the installation of [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

Als de viewer in configuratie werkt zoals aan het begin van deze sectie wordt beschreven, kan de gepubliceerde video zowel in de HTTPS-modus (beveiligd) als in de HTTP-modus (onveilig) worden afgespeeld. In een standaardconfiguratie, volgt het video leveringsprotocol strikt het leveringsprotocol van de het inbedden Web-pagina. Het is echter mogelijk om HTTPS-videoverzending te forceren zonder rekening te houden met het protocol dat wordt gebruikt door de webpagina in te sluiten met behulp van de [VideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e) configuratiekenmerk. (Voorvertoning van video in de modus Auteur wordt altijd veilig geleverd via HTTPS.)

Afhankelijk van de methode voor het publiceren van Dynamic Media-video die u in Adobe Experience Manager gebruikt, wordt de `VideoPlayer.ssl` configuratiekenmerk wordt anders toegepast, zoals in het volgende voorbeeld wordt getoond:

* Als u een Dynamic Media-video met een URL publiceert, voegt u `VideoPlayer.ssl` naar de URL. Als u bijvoorbeeld een beveiligde videoverzending wilt forceren, voegt u `&VideoPlayer.ssl=on` aan het einde van het volgende URL-voorbeeld voor de viewer:

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/MixedMediaViewer.html?asset=%2Fcontent%2Fdam%2FGeometrixx-Outdoors-New-Launch%2Fbackpack%2Fbackpack_mixed_media&config=/etc/dam/presets/viewer/MixedMedia_light&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&VideoPlayer.ssl=on
   ```

   Zie ook [(URL&#39;s koppelen aan uw webtoepassing)](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=en#dynamic).

* Als u een Dynamic Media-video met insluitcode publiceert, voegt u `VideoPlayer.ssl` aan de lijst van andere parameters van de kijkerconfiguratie in het inbedcodefragment. Als u bijvoorbeeld de HTTPS-video wilt afspelen, voegt u `&VideoPlayer.ssl=on` zoals in het volgende voorbeeld:

   ```
   <style type="text/css"> 
    #s7mixedmedia_div.s7mixedmediaviewer{ 
      width:100%;  
      height:auto; 
    } 
   </style> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/MixedMediaViewer.js"></script> 
   <div id="s7mixedmedia_div"></div> 
   <script type="text/javascript"> 
    var s7mixedmediaviewer = new s7viewers.MixedMediaViewer({ 
     "containerId" : "s7mixedmedia_div", 
     "params" : {  
      "VideoPlayer.ssl" : "on", 
      "serverurl" : "https://adobedemo62-h.assetsadobe.com/is/image", 
      "contenturl" : "https://demos-pub.assetsadobe.com/",  
      "config" : "/etc/dam/presets/viewer/MixedMedia_light", 
      "config2": "/etc/dam/presets/analytics", 
      "videoserverurl": "https://gateway-na.assetsadobe.com/DMGateway/public/demoCo", 
      "asset" : "/content/dam/Geometrixx-Outdoors-New-Launch/backpack/backpack_mixed_media" } 
    }).init(); 
   </script>
   ```

   Zie ook [(De video insluiten op een webpagina](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html#dynamic).
