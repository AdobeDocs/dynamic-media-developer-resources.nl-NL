---
description: Hiermee wordt een map verwijderd.
seo-description: Hiermee wordt een map verwijderd.
seo-title: deleteFolder
solution: Experience Manager
title: deleteFolder
uuid: 76af65fb-86ef-43e2-bfec-3682acf0afe6
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---


# deleteFolder{#deletefolder}

Hiermee wordt een map verwijderd.

Syntaxis

## Toegestane gebruikerstypen {#section-1c15a74c41194744a81f5ca86fe26585}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>De gebruiker moet lees- en verwijderrechten hebben voor de map en alle onderliggende bestanden.

## Parameters {#section-a793c98a481a4f26ab50bc69b16b57e7}

**Input (deleteFolderParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | De handgreep van het bedrijf waartoe de map behoort. |
| `*`folderHandle`*` | `xsd:string` | Ja | De handgreep van de map die moet worden verwijderd. |

**Output (deleteFolderParam)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-9d4617b322e8442d80e59be0f8714841}

Deze voorbeeldcode verwijdert een map uit de hoofdmap van het bedrijf. Hiervoor is een mapgreep vereist, die u moet verkrijgen van een andere bewerking.

**Verzoek**

```java
<ns1:deleteFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/SpinSets/</ns1:folderHandle>
</ns1:deleteFolderParam>
```

Geen.
