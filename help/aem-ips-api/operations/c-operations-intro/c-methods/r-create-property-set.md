---
description: Eigensets zijn toepassingsspecifieke sets van naam-waardeparen die aan verschillende IPS-objecten kunnen worden gekoppeld, afhankelijk van het type eigenschapset. Als het type eigenschapset niet toestaat dat meerdere sets aan een object kunnen worden gekoppeld (PropertySetType/allowMultipleisfalse) en het object al een gekoppelde set van hetzelfde type heeft, wordt de bestaande set vervangen.
solution: Experience Manager
title: createPropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: e9f85e65-4a2f-4b82-b7b8-d0d60b8345cd
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# createPropertySet{#createpropertyset}

Eigensets zijn toepassingsspecifieke sets van naam-waardeparen die aan verschillende IPS-objecten kunnen worden gekoppeld, afhankelijk van het type eigenschapset. Als het type eigenschapset niet toestaat dat meerdere sets aan een object kunnen worden gekoppeld (PropertySetType/allowMultipleisfalse) en het object al een gekoppelde set van hetzelfde type heeft, wordt de bestaande set vervangen.

Syntaxis

## Toegestane gebruikerstypen {#section-f9b6187ba636475787c997fc27bb192a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameters {#section-25258e75f5f3419bad165c797eb6cd8e}

**Input (createPropertySetParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`typeHandle`*` | `xsd:string` | Ja | De greep naar het type eigenschapset. |
| `*`primaryOwnerHandle`*` | `xsd:string` | Ja | De handgreep naar de primaire eigenaar van de eigenschapset. |
| `*`secundairOwnerHandle`*` | `xsd:string` | Nee | De handgreep naar de secundaire eigenaar van de eigenschapset. |
| `*`propertyArray`*` | `types:PropertyArray` | Ja | De array met eigenschappen. |
| `*`permissionArray`*` | `types:PermissionUpdateArray` |  |  |

**Output (createPropertySetParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`setHandle`*` | `xsd:string` | Ja | De greep naar de nieuwe eigenschapset. |

## Voorbeelden {#section-4e1f5b2883664bc88f590fcd253df22b}

In dit codevoorbeeld wordt een eigenschapset gemaakt die namen en waarden van eigenschappen bevat. De reactie keert een handvat aan de nieuwe bezitsreeks terug.

**Verzoek**

```java
<createPropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
   <primaryOwnerHandle>u|41|strangio@adobe.com</primaryOwnerHandle>
   <propertyArray>
      <items>
         <name>application_project_whatever</name>
         <value>true</value>
      </items>
      <items>
         <name>application_server_prefix_published_test</name>
         <value>http://s7everest.macromedia.com:8080/is/image/</value>
      </items>
      <items>
         <name>application_server_prefix_origin_test</name>
         <value>http://s7everest:8080/is/image/</value>
      </items>
   </propertyArray>
</createPropertySetParam>
```

**Antwoord**

```java
<createPropertySetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</createPropertySetReturn>
```
