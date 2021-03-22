---
description: Hiermee worden alle systeemeigenschappen in één aanvraag opgehaald.
seo-description: Hiermee worden alle systeemeigenschappen in één aanvraag opgehaald.
seo-title: getSystemProperties
solution: Experience Manager
title: getSystemProperties
uuid: 08ea86ba-bde5-45a1-920a-04f784395e6a
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 0%

---


# getSystemProperties{#getsystemproperties}

Hiermee worden alle systeemeigenschappen in één aanvraag opgehaald.

Syntaxis

## Toegestane gebruikerstypen {#section-fc311ce90a54400fa95b9dd36b756e23}

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

