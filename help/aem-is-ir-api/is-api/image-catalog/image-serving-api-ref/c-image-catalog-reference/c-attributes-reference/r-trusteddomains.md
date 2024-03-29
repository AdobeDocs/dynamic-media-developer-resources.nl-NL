---
description: Webdomeinen van de Flash-toepassing. Voor Adobe Flash-toepassingen is mogelijk toegang vereist tot de eigenschappen van afbeeldingen die worden geleverd met fmt=swf of fmt=swf3.
solution: Experience Manager
title: TrustedDomains
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 925ac9d1-203c-4814-a701-71060bf47c20
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---

# TrustedDomains{#trusteddomains}

Webdomeinen van de Flash-toepassing. Voor Adobe Flash-toepassingen is mogelijk toegang vereist tot de eigenschappen van afbeeldingen die worden geleverd met fmt=swf of fmt=swf3.

Het SWF-bestand moet expliciet toegang verlenen door de naam te registreren van de toepassingsdomeinen die het vertrouwt.

## Eigenschappen {#section-e7f95bbb749f441e83e90c2bc3d5a6e0}

Tekenreeks met een door komma&#39;s gescheiden lijst met webdomeinnamen. Als deze optie leeg is, moeten toepassingen worden aangeboden in hetzelfde domein als Afbeelding renderen om toegang te krijgen tot de eigenschappen van afbeeldingen in reacties met SWF-indeling.

## Standaard {#section-5c52ed3c7310488380f5a6f9540bf981}

Overgenomen van `default::TrustedDomains` indien niet aanwezig.

## Zie ook {#section-65d0846e41674882a4d0d56a8f6d524b}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
