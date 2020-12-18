---
description: Wijzigt de naam van een map.
seo-description: Wijzigt de naam van een map.
seo-title: renameFolder
solution: Experience Manager
title: renameFolder
topic: Scene7 Image Production System API
uuid: 7d190a57-1d81-4f41-9205-b8ffdf7330ec
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 0%

---


# renameFolder{#renamefolder}

Wijzigt de naam van een map.

Syntaxis

## Toegestane gebruikerstypen {#section-5a252b00937d4befbec76fa23fbae9df}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>De gebruiker moet lees- en schrijftoegang tot het element hebben.

## Parameters {#section-6fcee63dc3f74a5b90e1d71e59eb255c}

**Input (renameFolderParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Verwerk het bedrijf met mappen waarvan u de naam wilt wijzigen. |
| ` *`folderHandle`*` | `xsd:string` | Ja | Verwerk de map. |
| ` *`folderName`*` | `xsd:string` | Ja | Nieuwe mapnaam. |

**Output (naamMapReturn wijzigen)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`folderHandle`*` | `xsd:string` | Ja | Verwerk de map met gewijzigde namen. |

## Voorbeelden {#section-98bdd2f88d164f488676e90aba1dc864}

In dit codevoorbeeld wordt de naam van een map gewijzigd.

**Verzoek**

```java
<ns1:renameFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/PDF/</ns1:folderHandle>
   <ns1:folderName>My Newly Renamed PDF Folder</ns1:folderName>
</ns1:renameFolderParam>
```

**Antwoord**

```java
<renameFolderReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <folderHandle>MyCompany/My Newly Renamed PDF Folder/</folderHandle>
</renameFolderReturn>
```

