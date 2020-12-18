---
description: Werkt de setdefinitie voor een bestaande elementenset bij.
seo-description: Werkt de setdefinitie voor een bestaande elementenset bij.
seo-title: setAssetSetDefinition
solution: Experience Manager
title: setAssetSetDefinition
topic: Scene7 Image Production System API
uuid: 2a2dce5d-7a01-49af-ac8b-33ae0b234ecc
translation-type: tm+mt
source-git-commit: 55015831ed1971a305ddbd8085c95626507355e0
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---


# setAssetSetDefinition{#setassetsetdefinition}

Werkt de setdefinitie voor een bestaande elementenset bij.

Syntaxis

## Toegestane gebruikerstypen {#section-9d4ca3a8cfe74934b89971de01a2143c}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-c2057a5a13d042c684a3da1b49bc5dc6}

**Input (setAssetDefinitionParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | De handgreep aan het bedrijf met de activa reeks. |
| ` *`assetHandle`*` | `xsd:string` | Ja | Elementgreep |
| ` *`setDefinition`*` | `xsd:string` | Ja | Definitietekenreeks. Zie hieronder. |

**Output (setAssetSetDefinitionReturn)**

IPS API keert geen reactie voor deze verrichting terug.

## setDefinition-parameter: Info {#section-f88e066bf5294b4f8c12d5d652a5c94c}

**setDefinition-functies**

Geef `setDefinition` substitutiefuncties op in line. Deze worden opgelost tijdens het opzoeken van een catalogus of bij publicatie. Vervangende tekenreeksen hebben de notatie `${<substitution_func>}` en bevatten de volgende notaties:

>[!NOTE]
>
>Handle literals in de parameterlijsten moeten door haakjes `([])` worden omringd. De tekst buiten een vervangende tekenreeks wordt tijdens de resolutie naar de uitvoertekenreeks gekopieerd.

<table id="table_A93D2C273B694C289208AA926B2597CD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Vervangende functie </th> 
   <th colname="col2" class="entry"> Hiermee worden de elementen geretourneerd </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getFilePath([  <span class="varname"> asset_handle  </span>])  </span> </td> 
   <td colname="col2"> Primair bestandspad. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getCatalogd([  <span class="varname"> asset_handle  </span>])  </span> </td> 
   <td colname="col2"> Catalogus-id. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getMetaData([  <span class="varname"> asset_handle  </span>],[  <span class="varname"> metadata_field_handle  </span>])  </span> </td> 
   <td colname="col2"> Waarde van metagegevens. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getThumbCatalogId([  <span class="varname"> asset_handle  </span>])  </span> </td> 
   <td colname="col2"> Catalogus-id. Is van toepassing op op op afbeeldingen gebaseerde elementen (Afbeelding, Aangepaste weergave, Laagweergave). <p>Retourneert de catalogus-id van het blokelement (indien aanwezig) voor andere elementen. Als er geen blokelement aan het element is gekoppeld, retourneert de functie een lege tekenreeks. </p> </td> 
  </tr> 
 </tbody> 
</table>

**setDefinition Examples**

Deze mediaset als definitiereeks:

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])}; 
1,${getFilePath([a|1036|19|144])};${getCatalogId([a|452|1|433])};2; 
${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])}
```

Hiermee wordt het volgende bij het opzoeken of publiceren opgelost:

```java
jcompany/myRenderSet;jcompany/myRenderSet; 
1,jcompany/Videos/N08275_flv.flv;jcompany/myimg-1;2;20090703 10:05:53
```

## Voorbeelden {#section-739b42eec3074cafae285ec015a2d088}

**Verzoek**

```java
<setAssetSetDefinitionParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <companyHandle>c|1</companyHandle> 
   <assetHandle>a|1802|44|1802</assetHandle> 
   <setDefinition>${getCatalogId([a|1553|1|1176])};${getCatalogId([a|1553|1|1176])};1;img1, 
   ${getCatalogId([a|632|1|452])};${getCatalogId([a|632|1|452])};1,${getCatalogId([a|1664|22|1664])}; 
   ${getCatalogId([a|1664|22|1664])};1,${getFilePath([a|1036|19|144])};${getCatalogId([ a|452|1|433])}; 
   2;${getMetadata([a1036|19|144], [m|1|ASSET|SharedDateField])}</setDefinition> 
</setAssetSetDefinitionParam>
```

**Antwoord**

Geen.
