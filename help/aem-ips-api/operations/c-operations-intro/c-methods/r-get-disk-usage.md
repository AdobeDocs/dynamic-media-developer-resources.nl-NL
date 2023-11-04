---
description: Retourneert informatie over de structuur van een bedrijf (aantal bestanden, enzovoort.).
solution: Experience Manager
title: getDiskUsage
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 06fdd9f5-5021-4f0b-b312-4465df9bda25
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---

# getDiskUsage{#getdiskusage}

Retourneert informatie over de structuur van een bedrijf (aantal bestanden, enzovoort.).

## Geautoriseerde gebruikerstypen {#authorized-user-types}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameters {#section-e7e47082faf44ae28a2cfa7ef53aedbb}

**Input (getDiskUsageParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | De handgreep aan het bedrijf waarvan schijfgebruik u wilt verkrijgen. |

**Output (getDiskUsageReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| diskUsageArray | `types:DiskUsageArray` | Ja | Array van schijfgebruik van bedrijf. |

## Voorbeelden {#section-cb16a97badc94076ad5da277db5ed16a}

De naam van dit verzoek is misleidend. In plaats van alleen een scalaire waarde te retourneren die aangeeft hoeveel schijfruimte een bedrijf gebruikt, krijgt het ook andere informatie over de structuur van een bedrijf.

**Verzoek**

```java
<ns1:getDiskUsageParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getDiskUsageParam>
```

**Antwoord**

```java
<getDiskUsageReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <diskUsageArray>
      <items>
         <companyHandle>47</companyHandle>
         <companyName>My Company</companyName>
         <imageCount>207</imageCount>
         <diskSpaceUsage>3024</diskSpaceUsage>
         <lastModified>2007-09-14T22:10:30.661-07:00</lastModified>
      </items>
   </diskUsageArray>
</getDiskUsageReturn>
```
