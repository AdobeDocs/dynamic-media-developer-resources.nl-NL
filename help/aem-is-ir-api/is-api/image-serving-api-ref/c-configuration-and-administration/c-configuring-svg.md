---
description: De component SvgRender is een onafhankelijke Java-toepassing.
solution: Experience Manager
title: SVG configureren
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9013e13f-818f-41b4-80b6-2615d9a8742f
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 0%

---

# SVG configureren{#configuring-svg}

De component SvgRender is een onafhankelijke Java-toepassing.

SVG-configuratie-instellingen bevinden zich in [!DNL PlatformServer.conf], [!DNL SVG.conf], [!DNL ImageServerRegistry.xml], en [!DNL ServerSupervisorRegistry.xml].

Een contactdoosverbinding wordt gebruikt om tussen SvgRender en de Server van het Beeld te communiceren. Het poortnummer is 27346. Indien nodig kunt u deze wijzigen door `SVGRender.port` in [!DNL svg.conf] en `<SVGTcpPort>` in [!DNL ImageServerRegistry.xml] naar een nieuwe waarde.

## Zie ook {#section-c085b47d54d44059bdaa67fd5e226e91}

[SVG-configuratie-instellingen](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
