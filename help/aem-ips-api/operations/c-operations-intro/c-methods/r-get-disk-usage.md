---
description: Geeft informatie over de structuur van een bedrijf (aantal bestanden, enz.).
seo-description: Geeft informatie over de structuur van een bedrijf (aantal bestanden, enz.).
seo-title: getDiskUsage
solution: Experience Manager
title: getDiskUsage
topic: Scene7 Image Production System API
uuid: 29190200-8f49-4689-9782-1df665dca1b7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# getDiskUsage{#getdiskusage}

Geeft informatie over de structuur van een bedrijf (aantal bestanden, enz.).

## Toegestane gebruikerstypen {#authorized-user-types}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameters {#section-e7e47082faf44ae28a2cfa7ef53aedbb}

**Input (getDiskUsageParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | De handgreep aan het bedrijf waarvan schijfgebruik u wilt verkrijgen. |

**Output (getDiskUsageReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`diskUsageArray`*` | `types:DiskUsageArray` | Ja | Array van schijfgebruik van bedrijf. |

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

