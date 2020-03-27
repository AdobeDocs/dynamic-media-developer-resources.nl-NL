---
description: Stelt metagegevenswaarden in voor een element. Werkt met een array van updates van metagegevens om waarden in een batch in te stellen.
seo-description: Stelt metagegevenswaarden in voor een element. Werkt met een array van updates van metagegevens om waarden in een batch in te stellen.
seo-title: setAssetMetadata
solution: Experience Manager
title: setAssetMetadata
topic: Scene7 Image Production System API
uuid: 17fe8277-a164-4f91-af96-ea43d41bd4f2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAssetMetadata{#setassetmetadata}

Stelt metagegevenswaarden in voor een element. Werkt met een array van updates van metagegevens om waarden in een batch in te stellen.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-9dcacb0c924044648f8324bfed183dca}

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
| ` *`companyHandle`*` | `xsd:string` | Ja | De handgreep aan het bedrijf met de activa u wilt bijwerken. |
| ` *`assetHandle`*` | `xsd:string` | Ja | De handgreep van het element. |
| ` *`updateArray`*` | `types:MetadataUpdateArray` | Ja | Updates in een array met metagegevens bijwerken. |

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
