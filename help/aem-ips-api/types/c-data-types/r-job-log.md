---
description: Het taaklogboek nadat de taak is uitgevoerd.
solution: Experience Manager
title: JobLog
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 80ae6669-6fe7-45a6-9a1d-f8544dd4f878
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---

# JobLog{#joblog}

Het taaklogboek nadat de taak is uitgevoerd.

Syntaxis

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Naam | Type | Beschrijving |
|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Bedrijfshandgreep. |
| `*`jobHandle`*` | `xsd:string` | Taakgreep. |
| `*`jobName`*` | `xsd:string` | Taaknaam. |
| `*`originalJobName`*` | `xsd:string` | De oorspronkelijke naam die voor de taak is ingediend met `submitJob`. |
| `*`submitUserEmail`*` | `xsd:string` | Het e-mailadres van de gebruiker die de taak heeft verzonden. |
| `*`logType`*` | `xsd:string` | Keuze uit taaklogbestandstypen. |
| `*`jobSubType`*` | `xsd:string` | Aanvullende taakgegevens. |
| `*`startDate`*` | `xsd:dateTime` | De begindatum, tijd en tijdzone van de taak. |
| `*`endDate`*` | `xsd:dateTime` | De einddatum, tijd en tijdzone van de taak. |
| `*`beschrijving`*` | `xsd:string` | Een beschrijving van de taak zoals oorspronkelijk opgegeven in `submitJob`. |
| `*`fileSuccessCount`*` | `xsd:int` | Aantal bestanden verwerkt. |
| `*`fileErrorCount`*` | `xsd:int` | Aantal bestanden dat een fout heeft veroorzaakt. |
| `*`fileWarningCount`*` | `xsd:int` | Aantal bestanden dat een waarschuwing heeft gegenereerd. |
| `*`fileDuplicateCount`*` | `xsd:int` | Aantal gedupliceerde bestanden. |
| `*`fileUpdateCount`*` | `xsd:int` | Aantal bijgewerkte bestanden. |
| `*`totalFileCount`*` | `xsd:int` | Aantal bestanden dat door de geregistreerde taak is verwerkt. |
| `*`transferSuccessCount`*` | `xsd:int` | Aantal geslaagde overdrachten. |
| `*`transferErrorCount`*` | `xsd:int` | Aantal overdrachtsfouten. |
| `*`transferWarningCount`*` | `xsd:int` | Aantal overdrachtswaarschuwingen. |
| `*`fatalError`*` | `xsd:boolean` | Of de baan een fatale fout produceerde. |
| `*`detailTotalRows`*` | `xsd:int` | Het totale aantal rijen dat overeenkomt met de query. Dit kan groter zijn dan de grootte van `detailArray` vanwege de limieten van de paginagrootte. |
| `*`detailArray`*` | `types:JobLogDetailArray` | De array met details over de geregistreerde taak. |
