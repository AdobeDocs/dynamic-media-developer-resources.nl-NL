---
description: HTTP-videoboodsing
solution: Experience Manager
title: HTTP-videoboodsing
topic: Dynamic media
uuid: fd02a55a-a0f1-47a2-983f-15f296d1dbb4
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---


# HTTP-videoverzending{#http-video-delivery}

>[!NOTE]
>
>Beveiligde videoverlevering is alleen van toepassing op AEM 6.2 met de installatie van [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) en op AEM 6.1 met installatie van [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

Op voorwaarde dat de viewer in configuratie werkt zoals aan het begin van deze sectie wordt beschreven, kan de gepubliceerde video zowel in de HTTPS-modus (beveiligd) als in de HTTP-modus (onveilig) worden geleverd. In een standaardconfiguratie, volgt het video leveringsprotocol strikt het leveringsprotocol van de het inbedden Web-pagina. Het is echter mogelijk om HTTPS-videoverzending te forceren zonder rekening te houden met het protocol dat wordt gebruikt door de webpagina in te sluiten met het configuratiekenmerk [VideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e). (Videovoorvertoning in de modus Auteur wordt altijd veilig geleverd via HTTPS.)

Afhankelijk van de methode om de video van Dynamic Media te publiceren die u in AEM gebruikt, wordt `VideoPlayer.ssl` configuratieattributen toegepast verschillend zoals aangetoond in het volgende:

* Als u een Dynamic Media-video met een URL publiceert, voegt u `VideoPlayer.ssl` toe aan de URL. Als u bijvoorbeeld een beveiligde video wilt afspelen, voegt u `&VideoPlayer.ssl=on` toe aan het einde van het volgende URL-voorbeeld van de viewer:

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/VideoViewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Video&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&posterimage=/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4&VideoPlayer.ssl=on
   ```

   Zie ook [URLs aan uw Toepassing van het Web verbinden](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html).

* Als u een Dynamic Media-video met ingesloten code publiceert, voegt u `VideoPlayer.ssl` toe aan de lijst met andere parameters voor viewerconfiguratie in het ingesloten codefragment. Als u bijvoorbeeld de HTTPS-video wilt afspelen, voegt u `&VideoPlayer.ssl=on` toe, zoals in het volgende voorbeeld:

   ```
   <style type="text/css"> 
    #s7video_div.s7videoviewer{ 
      width:100%;  
      height:auto; 
    } 
   </style> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/VideoViewer.js"></script> 
   <div id="s7video_div"></div> 
   <script type="text/javascript"> 
    var s7videoviewer = new s7viewers.VideoViewer({ 
     "containerId" : "s7video_div", 
     "params" : {  
      "VideoPlayer.ssl" : "on", 
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

   Zie ook [De video insluiten op een webpagina](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html).

