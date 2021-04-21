---
description: Image Serving ondersteunt toegang tot bronafbeeldingen op externe HTTP- en FTP-servers.
solution: Experience Manager
title: Externe afbeeldingsbronnen
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---


# Externe afbeeldingsbronnen{#foreign-image-sources}

Image Serving ondersteunt toegang tot bronafbeeldingen op externe HTTP- en FTP-servers.

Een externe URL opgeven voor een opdracht `src=` of `mask=`; U kunt gewoon de volledige ingesloten URL met accolades afbakenen:

` …&src={ *[!DNL foreignUrl]*}&…`

Volledige absolute URL&#39;s (als `attribute::AllowDirectUrls` is ingesteld) en URL&#39;s ten opzichte van `attribute::RootUrl` zijn toegestaan. Er treedt een fout op als een absolute URL is ingesloten en een kenmerk: `AllowDirectUrls` is 0, of als een relatieve URL wordt gespecificeerd en `attribute::RootUrl` leeg is.

Externe afbeeldingen worden door de server in het cachegeheugen opgeslagen volgens de headers die bij de HTTP-respons worden geleverd.
