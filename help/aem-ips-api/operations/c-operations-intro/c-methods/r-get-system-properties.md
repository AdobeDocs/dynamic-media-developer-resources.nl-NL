---
description: Hiermee worden alle systeemeigenschappen in één aanvraag opgehaald.
solution: Experience Manager
title: getSystemProperties
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: b0ef16fd-1645-4e22-99bb-8c9269623168
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 0%

---

# getSystemProperties{#getsystemproperties}

Hiermee worden alle systeemeigenschappen in één aanvraag opgehaald.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-fc311ce90a54400fa95b9dd36b756e23}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`
* `TrialSiteAdmin`
* `TrialSiteUser`

## Parameters {#section-b2a4fb7068424223aec87c50f0586d73}

**Input (getSystemPropertiesParam)**

Geen.

**Output (getSystemPropertiesReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`propertyArray`*` | `types:PropertyArray` | Ja | Een array met systeemeigenschappen. |

## Voorbeelden {#section-728cc16fe9954b2daa035b4d4d4b4ce6}

Deze codesteekproef keert een serie van systeemeigenschappen terug. Respons ingekort voor bondigheid.

**Verzoek**

```java
<getSystemPropertiesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10"/>
```

**Antwoord**

```java
<getSystemPropertiesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10"> 
   <propertyArray> 
      <items> 
         <name>SvgRenderEnabled</name> 
         <value>true</value> 
      </items> 
      <items> 
         <name>SwfRootUrl</name> 
         <value>/SWFs/</value> 
      </items> 
      ... 
   </propertyArray> 
</getSystemPropertiesReturn>
```
