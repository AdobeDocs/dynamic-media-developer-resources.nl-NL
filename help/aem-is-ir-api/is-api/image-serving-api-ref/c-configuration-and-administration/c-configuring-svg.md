---
description: De component SvgRender is een onafhankelijke Java-toepassing.
seo-description: De component SvgRender is een onafhankelijke Java-toepassing.
seo-title: SVG configureren
solution: Experience Manager
title: SVG configureren
topic: Scene7 Image Serving - Image Rendering API
uuid: f6e131af-283e-4649-b349-123489c0838d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SVG configureren{#configuring-svg}

De component SvgRender is een onafhankelijke Java-toepassing.

De de configuratiemontages van SVG worden gevestigd in [!DNL PlatformServer.conf], [!DNL SVG.conf], [!DNL ImageServerRegistry.xml], en [!DNL ServerSupervisorRegistry.xml].

Een contactdoosverbinding wordt gebruikt om tussen SvgRender en de Server van het Beeld te communiceren. Het poortnummer is 27346. Indien nodig kunt u de waarde wijzigen door `SVGRender.port` in [!DNL svg.conf] en `<SVGTcpPort>` in [!DNL ImageServerRegistry.xml] te stellen op een nieuwe waarde.

## Zie ook {#section-c085b47d54d44059bdaa67fd5e226e91}

[SVG-configuratie-instellingen](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
