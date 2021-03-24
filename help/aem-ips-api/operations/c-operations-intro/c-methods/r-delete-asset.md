---
description: Hiermee verwijdert u een element.
solution: Experience Manager
title: deleteAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---


# deleteAsset{#deleteasset}

Hiermee verwijdert u een element.

Syntaxis

## Toegestane gebruikerstypen {#section-e913be43b684491daf02bc73211e4290}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>De gebruiker moet lees- en verwijdertoegang tot het element hebben.

## Parameters {#section-0eed164e278b456fbdfb7a50727a0416}

**Input (deleteAssetParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | De handgreep van het bedrijf waartoe de map behoort. |
| `*`assetHandle`*` | `xsd:string` | Ja | De handgreep van het element dat moet worden verwijderd. |

**Uitvoer (deleteAssetParam)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-d5657289f5234bb0a613dcf691507958}

Met deze voorbeeldcode verwijdert u elk type element van een bepaald bedrijf. Hiervoor is een elementhandgreep vereist, die u moet verkrijgen van een andere bewerking.

**Verzoek**

```java
<ns1:deleteAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
</ns1:deleteAssetParam>
```

**Antwoord**

Geen.
