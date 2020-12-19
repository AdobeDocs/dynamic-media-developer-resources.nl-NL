---
description: Hiermee wordt een array met leden opgehaald die zich in een afbeeldingsset bevinden.
seo-description: Hiermee wordt een array met leden opgehaald die zich in een afbeeldingsset bevinden.
seo-title: getImageSetMember
solution: Experience Manager
title: getImageSetMember
topic: Scene7 Image Production System API
uuid: b19c9fec-df92-42e1-9228-42cdf196fdfc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---


# getImageSetmembers{#getimagesetmembers}

Hiermee wordt een array met leden opgehaald die zich in een afbeeldingsset bevinden.

Syntaxis

## Toegestane gebruikerstypen {#section-eaa3a167fa77403ea1b374b05fff4ded}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Vereist leestoegang tot het beeld en lid vastgestelde element.

## Parameters {#section-a67ba98095574533980997c83ceaa316}

**Input (getImageSetMemberParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | De handgreep naar het bedrijf dat de afbeeldingsset bevat. |
| ` *`assetHandle`*` | `xsd:string` | Ja | De greep voor de afbeeldingsset met elementen. |

**Output (getImageSetMemberReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`memberArray`*` | `types:ImageSetMemberArray` | Nee | Array met leden van afbeeldingssets. |

## Voorbeelden {#section-888a9a78033346f39b171229de93dfa0}

Dit codevoorbeeld retourneert specifieke leden van een afbeeldingsset. De reactie retourneert een lege array.

**Verzoek**

```java
<ns1:getImageSetMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>34195|22|927</ns1:assetHandle>
</ns1:getImageSetMembersParam>
```

**Antwoord**

```java
<getImageSetMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <memberArray></memberArray>
</getImageSetMembersReturn>
```

