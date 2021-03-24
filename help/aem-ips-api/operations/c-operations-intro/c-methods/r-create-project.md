---
description: Hiermee maakt u een nieuw project.
solution: Experience Manager
title: createProject
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# createProject{#createproject}

Hiermee maakt u een nieuw project.

Syntaxis

## Toegestane gebruikerstypen {#section-17878e2e4c3a44988c9a1af82c2ac319}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-8c741884eb54489bbaad0c444fee80b6}

**Input (createProjectParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | De handgreep van het bedrijf verbonden aan het nieuwe project. |
| `*`projectName`*` | `xsd:string` | Ja | Nieuwe projectnaam. |

**Uitvoer (createProjectParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`projectHandle`*` | `xsd:string` | Ja | De greep naar het nieuwe project. |

## Voorbeelden {#section-a0cd532b67e346d088fbec141231a0e5}

Deze codesteekproef leidt tot een project genoemd `ApiTestProject` in een bedrijf door zijn handvat wordt gespecificeerd. De reactie keert de handvat aan het project terug.

**Verzoek**

```java
<createProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectName>ApiTestProject</projectName>
</createProjectParam>
```

```java
<createProjectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <projectHandle>p|6|ApiTestProject</projectHandle>
</createProjectReturn>
```

