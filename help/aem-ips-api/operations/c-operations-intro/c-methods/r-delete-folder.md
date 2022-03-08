---
description: Hiermee wordt een map verwijderd.
solution: Experience Manager
title: deleteFolder
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c042b87b-3f60-4608-8ed5-0fc031a66c03
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# deleteFolder{#deletefolder}

Hiermee wordt een map verwijderd.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-1c15a74c41194744a81f5ca86fe26585}

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
| companyHandle | `xsd:string` | Ja | De handgreep van het bedrijf waartoe de map behoort. |
| folderHandle | `xsd:string` | Ja | De handgreep van de map die moet worden verwijderd. |

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
