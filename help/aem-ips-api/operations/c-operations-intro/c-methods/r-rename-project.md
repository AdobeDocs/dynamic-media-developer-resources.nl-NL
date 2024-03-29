---
description: Wijzigt de naam van een project.
solution: Experience Manager
title: renameProject
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 1bf74ebf-1fce-408b-9953-7fdf2ae9d10b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 0%

---

# renameProject{#renameproject}

Wijzigt de naam van een project.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-093d1f611a1647568e885ddd842b8f78}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-43ccd77648784be4a259a723c3e1db40}

**Input (renameProjectParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| companyName | `xsd:string` | Ja | Handvat aan het bedrijf met het project u wilt anders noemen. |
| projectHandle | `xsd:string` | Ja | Handgreep aan het project. |
| projectName | `xsd:string` | Ja | Nieuwe projectnaam. |

**Uitvoer (naamProjectParam wijzigen)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| projectHandle | `xsd:string` | Ja | De greep van het anders genoemde project. |

## Voorbeelden {#section-a0a06d9244774795b695a10b92b2a5e7}

Deze codesteekproef anders noemt een project en keert de projecthandvat terug.

**Verzoek**

```java
<renameProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ApiTestProject</projectHandle>
   <projectName>ProjectTestAPI</projectName>
</renameProjectParam>
```

**Antwoord**

```java
<renameProjectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
</renameProjectReturn>
```
