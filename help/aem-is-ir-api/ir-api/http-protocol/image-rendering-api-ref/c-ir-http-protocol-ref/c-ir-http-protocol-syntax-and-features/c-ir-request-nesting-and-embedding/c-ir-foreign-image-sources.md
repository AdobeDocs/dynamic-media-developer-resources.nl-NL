---
title: Externe afbeeldingsbronnen
description: Image Serving ondersteunt toegang tot bronafbeeldingen op externe HTTP- en FTP-servers.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90f96a76-e9f3-4ad0-84af-bc0d093acf19
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---

# Externe afbeeldingsbronnen{#foreign-image-sources}

Image Serving ondersteunt toegang tot bronafbeeldingen op externe HTTP- en FTP-servers.

Een externe URL opgeven voor een `src=` of `mask=` bevel; U kunt gewoon de volledige ingesloten URL met accolades afbakenen:

` …&src={ *[!DNL foreignUrl]*}&…`

Volledige absolute URL&#39;s (als `attribute::AllowDirectUrls` is ingesteld) en URL&#39;s ten opzichte van `attribute::RootUrl` zijn toegestaan. Er treedt een fout op als een absolute URL is ingesloten en een kenmerk: `AllowDirectUrls` is 0 of als een relatieve URL is opgegeven en `attribute::RootUrl` is leeg.

Externe afbeeldingen worden door de server in het cachegeheugen opgeslagen volgens de headers die bij de HTTP-respons worden geleverd.
