---
description: De component SvgRender is een onafhankelijke Java-toepassing.
solution: Experience Manager
title: SVG configureren
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 0%

---


# SVG{#configuring-svg} configureren

De component SvgRender is een onafhankelijke Java-toepassing.

SVG-configuratie-instellingen bevinden zich in [!DNL PlatformServer.conf], [!DNL SVG.conf], [!DNL ImageServerRegistry.xml] en [!DNL ServerSupervisorRegistry.xml].

Een contactdoosverbinding wordt gebruikt om tussen SvgRender en de Server van het Beeld te communiceren. Het poortnummer is 27346. Indien nodig, kan het worden veranderd door `SVGRender.port` in [!DNL svg.conf] en `<SVGTcpPort>` in [!DNL ImageServerRegistry.xml] in een nieuwe waarde te plaatsen.

## Zie ook {#section-c085b47d54d44059bdaa67fd5e226e91}

[SVG-configuratie-instellingen](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
