---
description: Maakt een map.
seo-description: Maakt een map.
seo-title: createFolder
solution: Experience Manager
title: createFolder
topic: Scene7 Image Production System API
uuid: e3a4eed3-966d-4435-bfeb-3ead4bf523cd
translation-type: tm+mt
source-git-commit: d64337d3ed7bd78c681c3022cda20012726d7ccc
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---


# [!DNL createFolder]{#createfolder}

Maakt een map.

>[!NOTE]
>
>De nieuwe map is ondergeschikt aan de map Images, zelfs als u een `/` opgeeft om de hoofdmap van het bedrijf aan te geven.

Syntaxis

## Toegestane gebruikerstypen {#section-14ef6368056b4e8f96198c20b6d93b9b}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>De gebruiker moet lees-/schrijftoegang tot de bovenliggende map hebben.

## Parameters {#section-c00d8d89cf114886a535056f2a1bf892}

**Invoer (createFolder)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | De handgreep aan het bedrijf |
| ` *`folderPath`*` | `xsd:string` | Ja | De hoofdmap die wordt gebruikt om mappen en alle submappen op bladniveau op te halen. Indien uitgesloten, wordt de bedrijfwortel gebruikt. |

**Uitvoer (createFolderParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`folderHandle`*` | `xsd:string` | Ja | Handgreep van de nieuwe map. |

## Voorbeelden {#section-e596fbdb44fd43c8b30005cb2a2fdf26}

Deze voorbeeldcode leidt tot een omslag bij de wortel van een bedrijf. De reactie retourneert de greep van de nieuwe map.

**Verzoek**

```java
<ns1:createFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderPath>/SpinSets</ns1:folderPath>
</ns1:createFolderParam>
```

**Antwoord**

```java
<ns1:createFolderReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <folderHandle xmlns="http://www.scene7.com/IpsApi/xsd">MyCompany/SpinSets/</folderHandle>
</ns1:createFolderReturn>
```

