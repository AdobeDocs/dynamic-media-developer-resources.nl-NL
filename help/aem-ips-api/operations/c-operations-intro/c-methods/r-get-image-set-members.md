---
description: Hiermee wordt een array met leden opgehaald die zich in een afbeeldingsset bevinden.
solution: Experience Manager
title: getImageSetMember
feature: Dynamic Media Classic,SDK/API,Afbeeldingssets
role: Developer,Admin
exl-id: 29ceef8b-127f-4460-8623-c3e26c959327
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---

# getImageSetMember{#getimagesetmembers}

Hiermee wordt een array met leden opgehaald die zich in een afbeeldingsset bevinden.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-eaa3a167fa77403ea1b374b05fff4ded}

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
| `*`companyHandle`*` | `xsd:string` | Ja | De handgreep naar het bedrijf dat de afbeeldingsset bevat. |
| `*`assetHandle`*` | `xsd:string` | Ja | De greep voor de afbeeldingsset met elementen. |

**Output (getImageSetMemberReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`memberArray`*` | `types:ImageSetMemberArray` | Nee | Array met leden van afbeeldingssets. |

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
