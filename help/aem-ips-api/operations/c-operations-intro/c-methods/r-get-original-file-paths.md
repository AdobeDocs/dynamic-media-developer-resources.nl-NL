---
description: Haalt de oorspronkelijke bestandspaden van de elementen van een bedrijf op.
seo-description: Haalt de oorspronkelijke bestandspaden van de elementen van een bedrijf op.
seo-title: getOriginalFilePaths
solution: Experience Manager
title: getOriginalFilePaths
topic: Scene7 Image Production System API
uuid: c4acf288-1a57-4295-806b-348f15a089cc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getOriginalFilePaths{#getoriginalfilepaths}

Haalt de oorspronkelijke bestandspaden van de elementen van een bedrijf op.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-da8d8561e9174e938f3595a5d6e50089}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Vereist leestoegang tot het middel.

## Parameters {#section-a6b394daba6e49a8882cf3051035d9d1}

**Input (getOriginalFilePathsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | De handgreep aan het bedrijf. |
| ` *`assetHandleArray`*` | `types:HandleArray` | Ja | Array van handgrepen naar elementen waarvan u het oorspronkelijke bestandspad wilt verkrijgen. |

**Output (getOriginalFilePathsReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`originalFileArray`*` | `types:StringArray` | Ja | De array van tekenreeksen die staan voor de oorspronkelijke bestandspaden. |

## Voorbeelden {#section-a966e783a2ba49f5b6b0f961329ab2f8}

Dit codevoorbeeld retourneert de bestandspaden van elementen die zijn opgegeven met unieke elementhandgrepen in een elementgreep-array.

**Verzoek**

```java
<ns1:getOriginalFilePathsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandleArray>
      <ns1:items>24265|1|17061</ns1:items>
      <ns1:items>24267|1|17063</ns1:items>
   </ns1:assetHandleArray>
</ns1:getOriginalFilePathsParam>
```

**Antwoord**

```java
<getOriginalFilePathsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <originalFileArray>
      <items>MyCompany/Autumn Leaves.jpg</items>
      <items>MyCompany/Desert Landscape.jpg</items>
   </originalFileArray>
</getOriginalFilePathsReturn>
```

