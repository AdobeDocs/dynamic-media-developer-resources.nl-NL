---
description: Stelt metagegevenswaarden in voor een element. Werkt met een array van updates van metagegevens om waarden in een batch in te stellen.
solution: Experience Manager
title: setAssetMetadata
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 0%

---


# setAssetMetadata{#setassetmetadata}

Stelt metagegevenswaarden in voor een element. Werkt met een array van updates van metagegevens om waarden in een batch in te stellen.

Syntaxis

## Toegestane gebruikerstypen {#section-9dcacb0c924044648f8324bfed183dca}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>De gebruiker moet lees toegang tot het middel hebben.

## Parameters {#section-bcdcff30905e444388811e897b2824bd}

**Input (setAssetMetadataParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | De handgreep aan het bedrijf met de activa u wilt bijwerken. |
| `*`assetHandle`*` | `xsd:string` | Ja | De handgreep van het element. |
| `*`updateArray`*` | `types:MetadataUpdateArray` | Ja | Updates in een array met metagegevens bijwerken. |

**Output (setAssetMetadataReturn)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-1ab412e7ee1d4d6d8469b0b403598c42}

In dit codevoorbeeld wordt een array met updates van metagegevens gebruikt om de metagegevens van het opgegeven element in te stellen.

**Verzoek**

```java
<ns1:setAssetMetadataParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
   <ns1:updateArray>
      <ns1:items>
         <ns1:fieldHandle>47|ALL|Resolution</ns1:fieldHandle>
         <ns1:value>320</ns1:value>
      </ns1:items>
   </ns1:updateArray>
</ns1:setAssetMetadataParam>
```

**Antwoord**

Geen.
