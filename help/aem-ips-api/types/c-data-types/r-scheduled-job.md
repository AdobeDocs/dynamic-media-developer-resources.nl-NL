---
description: Een taak die volgens planning moet worden uitgevoerd.
seo-description: Een taak die volgens planning moet worden uitgevoerd.
seo-title: ScheduledJob
solution: Experience Manager
title: ScheduledJob
topic: Scene7 Image Production System API
uuid: cf0db523-2138-48c6-abbd-460a961e7de1
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 0%

---


# ScheduledJob{#scheduledjob}

Een taak die volgens planning moet worden uitgevoerd.

Syntaxis

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Naam | Type | Beschrijving |
|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Bedrijfshandgreep. |
| ` *`jobHandle`*` | `xsd:string` | Geplande taakgreep. |
| ` *`name`*` | `xsd:string` | Taaknaam. |
| ` *`originalName`*` | `xsd:string` | Oorspronkelijke naam van de geplande taak. |
| ` *`type`*` | `xsd:string` | Taaktype. |
| ` *`submitUserEmail`*` | `xsd:string` | Het e-mailadres van de gebruiker die de taak heeft gepland. |
| ` *`landinstelling`*` | `xsd:string` | De landinstelling die moet worden gebruikt voor loggegevens van taken en e-maillokalisatie. Landinstellingen worden opgegeven als `<language_code>[- <country_code>]`, waarbij de taalcode een code van twee kleine letters is zoals gespecificeerd in ISO-639, en de optionele landcode een code van twee letters in hoofdletters is zoals gespecificeerd in ISO-3166. De landinstelling voor Engels (Verenigde Staten) zou bijvoorbeeld als volgt zijn: `en-US`. |
| ` *`beschrijving`*` | `xsd:string` | Een beschrijving van de taak zoals oorspronkelijk opgegeven in `submitJob`. |
| ` *`execSchedule`*` | `xsd:string` | Wanneer de taak volgens planning moet worden uitgevoerd. |
| ` *`nextFireTime`*` | `xsd:dateTime` | De datum, tijd en tijdzone waarop de taak wordt gestart. |
| ` *`timeZone`*` | `xsd:dateTime` | De tijdzone van de geplande taak. |
| ` *`triggerState`*` | `xsd:int` | Keuze van status voor taaktrigger. |
| ` *`imageServingPublishJob`*` | `types:ImageServingPublishJob` | Taakdetails voor een afbeelding die publicatietaak aanbiedt. |
| ` *`imageServingRenderJob`*` | `types:ImageServingRenderJob` | Taakdetails voor een renderingtaak voor afbeeldingen. |
| ` *`videoPublishJob`*` | `types:VideoPublishJob` | Taakdetails voor een video-publicatietaak. Zie [VideoPublishJob](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html). |
| ` *`serverDirectoryPublishJob`*` | `types:ServerDirectoryPublishJob` | Taakgegevens voor de publicatietaak van een servermap. |
| ` *`uploadDirectoryJob`*` | `types:UploadDirectoryJob` | Taakgegevens voor een uploadmaptaak. |
| ` *`uploadUrlsJob`*` | `types:UploadUrlsJob` | Taakgegevens voor een upload-URL&#39;s-taak. |
| ` *`optimizeImagesJob`*` | `types:OptimizeImagesJob` |  |
| ` *`ripPdfsJob`*` | `types:RipPdfsJob` |  |
| ` *`reprocessAssetsJob`*` | `types:ReprocessAssetsJob` |  |
| ` *`exportJob`*` | `types:ExportJob` | Toestaan dat eerder geüploade bestanden zijn geëxporteerd. Zie [Taak exporteren](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html). |

## Notities {#section-34ec157f281f412f9f0f6e861e6ed0cd}

Wanneer u een taaktypewaarde opgeeft in `submitJob`, retourneert het systeem een taak op basis van dat type. De volgende taken kunnen worden geretourneerd:

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectorhJob`
* `uploadUrlsJob`

