---
description: Hiermee maakt u een nieuw project.
solution: Experience Manager
title: createProject
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dd9c07df-9a8f-4b67-9838-31dd96fd127b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---

# createProject{#createproject}

Hiermee maakt u een nieuw project.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-17878e2e4c3a44988c9a1af82c2ac319}

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
| companyHandle | `xsd:string` | Ja | De handgreep van het bedrijf verbonden aan het nieuwe project. |
| projectName | `xsd:string` | Ja | Nieuwe projectnaam. |

**Uitvoer (createProjectParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| projectHandle | `xsd:string` | Ja | De greep naar het nieuwe project. |

## Voorbeelden {#section-a0cd532b67e346d088fbec141231a0e5}

Dit codevoorbeeld leidt tot een project genoemd `ApiTestProject` in een bedrijf dat door zijn greep wordt gespecificeerd. De reactie keert de handvat aan het project terug.

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
