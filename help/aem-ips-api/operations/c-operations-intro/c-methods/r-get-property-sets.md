---
description: Hiermee worden eigenschapssets opgehaald die aan een tekstgreep zijn gekoppeld.
solution: Experience Manager
title: getPropertySets
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: da6923c3-9b86-4595-8205-645fb10e03b0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---

# getPropertySets{#getpropertysets}

Hiermee worden eigenschapssets opgehaald die aan een tekstgreep zijn gekoppeld.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-da858360b72941bfa8d9558b4da7d4da}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-d8da2847e77e4a95a4441d9848cac775}

**Input (getPropertySetsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| typeHandle | `xsd:string` | Ja | De greep naar het type eigenschapset. |
| primaryOwnerHandle | `xsd:string` | Ja | De primaire eigenaar van de gegevens die aan het databaseobject zijn gebonden. |
| secundairOwnerHandle | `xsd:string` | Nee | Een optionele secundaire eigenaar van de gegevens. |

**Output (getPropertySetsReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| setArray | `types:PropertySetArray` | Ja | Array met eigenschapssets. |

## Voorbeelden {#section-1358af974eab4259864910337a6f0bd2}

Deze codesteekproef keert bezitsreeksen van hun primaire eigenaar terug, die door een typehandvat wordt gespecificeerd.

**Verzoek**

```java
<getPropertySetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
   <primaryOwnerHandle>u|41|strangio@adobe.com</primaryOwnerHandle>
</getPropertySetsParam>
```

**Antwoord**

```java
<getPropertySetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setArray>
      <items>
         <setHandle>ps|941</setHandle>
         <typeHandle>pt|10801</typeHandle>
         <propertyArray>
            <items>
               <name>application_server_prefix_published_test</name>
               <value>http://s7teton.macromedia.com:8080/is/image/</value>
            </items>
            <items>
               <name>application_project_whatever</name>
               <value>false</value>
            </items>
            <items>
               <name>application_server_prefix_origin_test</name>
               <value>http://s7teton:8080/is/image</value>
            </items>
         </propertyArray>
      </items>
   </setArray>
</getPropertySetsReturn>
```
