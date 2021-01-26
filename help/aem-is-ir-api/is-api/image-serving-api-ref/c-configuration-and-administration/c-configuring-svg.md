---
description: De component SvgRender is een onafhankelijke Java-toepassing.
seo-description: De component SvgRender is een onafhankelijke Java-toepassing.
seo-title: SVG configureren
solution: Experience Manager
title: SVG configureren
topic: Dynamic Media Image Serving - Image Rendering API
uuid: f6e131af-283e-4649-b349-123489c0838d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 0%

---


# SVG{#configuring-svg} configureren

De component SvgRender is een onafhankelijke Java-toepassing.

SVG-configuratie-instellingen bevinden zich in [!DNL PlatformServer.conf], [!DNL SVG.conf], [!DNL ImageServerRegistry.xml] en [!DNL ServerSupervisorRegistry.xml].

Een contactdoosverbinding wordt gebruikt om tussen SvgRender en de Server van het Beeld te communiceren. Het poortnummer is 27346. Indien nodig, kan het worden veranderd door `SVGRender.port` in [!DNL svg.conf] en `<SVGTcpPort>` in [!DNL ImageServerRegistry.xml] in een nieuwe waarde te plaatsen.

## Zie ook {#section-c085b47d54d44059bdaa67fd5e226e91}

[SVG-configuratie-instellingen](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
