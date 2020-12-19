---
description: Image Serving ondersteunt toegang tot bronafbeeldingen op externe HTTP- en FTP-servers.
seo-description: Image Serving ondersteunt toegang tot bronafbeeldingen op externe HTTP- en FTP-servers.
seo-title: Externe afbeeldingsbronnen
solution: Experience Manager
title: Externe afbeeldingsbronnen
topic: Scene7 Image Serving - Image Rendering API
uuid: 28a17400-4807-4e14-937a-80309be53d55
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---


# Externe afbeeldingsbronnen{#foreign-image-sources}

Image Serving ondersteunt toegang tot bronafbeeldingen op externe HTTP- en FTP-servers.

Een externe URL opgeven voor een opdracht `src=` of `mask=`; U kunt gewoon de volledige ingesloten URL met accolades afbakenen:

` …&src={ *[!DNL foreignUrl]*}&…`

Volledige absolute URL&#39;s (als `attribute::AllowDirectUrls` is ingesteld) en URL&#39;s ten opzichte van `attribute::RootUrl` zijn toegestaan. Er treedt een fout op als een absolute URL is ingesloten en een kenmerk: `AllowDirectUrls` is 0, of als een relatieve URL wordt gespecificeerd en `attribute::RootUrl` leeg is.

Externe afbeeldingen worden door de server in het cachegeheugen opgeslagen volgens de headers die bij de HTTP-respons worden geleverd.
