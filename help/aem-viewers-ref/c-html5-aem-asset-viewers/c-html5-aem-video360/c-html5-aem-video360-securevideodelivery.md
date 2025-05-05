---
title: HTTPS-video leveren
description: HTTPS-video leveren
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 79f7e356-55d1-46e1-b85a-2e73633c9404
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# HTTPS-video leveren{#https-video-delivery}

<!-- >[!NOTE]
>
>HTTP Secure Video Delivery applies only to AEM 6.2 with the installation of [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

Als de viewer in configuratie werkt zoals aan het begin van deze sectie wordt beschreven, kan de gepubliceerde video zowel in de HTTPS-modus (beveiligd) als in de HTTP-modus (onveilig) worden afgespeeld. In een standaardconfiguratie, volgt het video leveringsprotocol strikt het leveringsprotocol van de het inbedden Web-pagina. Het is echter mogelijk om HTTPS-videoverzending te forceren zonder rekening te houden met het protocol dat wordt gebruikt door de webpagina in te sluiten met behulp van de [Video360Player.ssl](/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-video360/r-html5-aem-video360-config-attrib/r-html5-aem-video360-config-attrib-video360player-ssl.md) configuratiekenmerk. (Voorvertoning van video in de modus Auteur wordt altijd veilig geleverd via HTTPS.)

Afhankelijk van de methode voor het publiceren van Dynamic Media-video die u in Adobe Experience Manager gebruikt, wordt de `Video360Player.ssl` configuratiekenmerk wordt anders toegepast, zoals in het volgende voorbeeld wordt getoond:

* Als u een Dynamic Media-video met een URL publiceert, voegt u `Video360Player.ssl` naar de URL. Als u bijvoorbeeld een beveiligde videoverzending wilt forceren, voegt u `&Video360Player.ssl=on` aan het einde van het volgende URL-voorbeeld voor de viewer:

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/Video360Viewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Video&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&posterimage=/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4&Video360Player.ssl=on
   ```

   Zie ook [URL&#39;s koppelen aan uw webtoepassing](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=nl-NL#dynamic).

* Als u een Dynamic Media-video met insluitcode publiceert, voegt u `Video360Player.ssl` aan de lijst van andere parameters van de kijkerconfiguratie in het inbedcodefragment. Als u bijvoorbeeld de HTTPS-video wilt afspelen, voegt u `&Video360Player.ssl=on` zoals in het volgende voorbeeld:

   ```
   <style type="text/css"> 
    #s7video_div.s7video360viewer{ 
      width:100%;  
      height:auto; 
    } 
   </style> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js"></script> 
   <div id="s7video_div"></div> 
   <script type="text/javascript"> 
    var s7video360viewer = new s7viewers.Video360Viewer({ 
     "containerId" : "s7video_div", 
     "params" : {  
      "Video360Player.ssl" : "on", 
      "serverurl" : "https://adobedemo62-h.assetsadobe.com/is/image", 
      "contenturl" : "https://demos-pub.assetsadobe.com/",  
      "config" : "/etc/dam/presets/viewer/Video", 
      "config2": "/etc/dam/presets/analytics", 
      "videoserverurl": "https://gateway-na.assetsadobe.com/DMGateway/public/demoCo", 
      "posterimage": "/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4", 
      "asset" : "/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4" } 
    }).init(); 
   </script>
   ```

   Zie ook [De video insluiten op een webpagina](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=nl-NL#dynamic)
