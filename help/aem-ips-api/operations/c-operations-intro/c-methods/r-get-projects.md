---
description: Hiermee worden projecten opgehaald voor een groep gerelateerde activa.
seo-description: Hiermee worden projecten opgehaald voor een groep gerelateerde activa.
seo-title: getprojects
solution: Experience Manager
title: getprojects
uuid: 46ec9a5d-4414-4c9c-aaf2-0db654204b61
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 0%

---


# getProjecten{#getprojects}

Hiermee worden projecten opgehaald voor een groep gerelateerde activa.

Syntaxis

## Toegestane gebruikerstypen {#section-337649866b1f4098844d1974ed7ab5d0}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-8d549237b8c440b4872a0a086ddc00a1}

**Input (getprojectsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | De handgreep aan het bedrijf. |

**Output (getprojectsReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`projectArray`*` | `types:ProjectArray` | Ja | De serie van projecten verbonden aan het bedrijf. |

## Voorbeelden {#section-8b12d0b948f644f68bf9a16060d3849a}

Deze codesteekproef keert alle projecthandvatten in een projectserie terug.

**Verzoek**

```java
<ns1:getProjectsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getProjectsParam>
```

**Antwoord**

```java
<getProjectsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <projectArray>
      <items>
         <projectHandle>47|My Project 1</projectHandle>
         <name>My Project 1</name>
      </items>
      <items>
         <projectHandle>47|My Project 2</projectHandle>
         <name>My Project 2</name>
      </items>
   </projectArray>
</getProjectsReturn>
```

