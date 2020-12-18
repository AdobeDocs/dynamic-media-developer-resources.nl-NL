---
description: Creeert een generisch element dat met een ruwe reeks definitiekoord wordt geplaatst dat aan een Server van het Beeld moet worden gepubliceerd.
seo-description: Creeert een generisch element dat met een ruwe reeks definitiekoord wordt geplaatst dat aan een Server van het Beeld moet worden gepubliceerd.
seo-title: createAssetSet
solution: Experience Manager
title: createAssetSet
topic: Scene7 Image Production System API
uuid: 1e86bd37-511c-4c12-abfd-075053b86f78
translation-type: tm+mt
source-git-commit: 55015831ed1971a305ddbd8085c95626507355e0
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 0%

---


# createAssetSet{#createassetset}

Creeert een generisch element dat met een ruwe reeks definitiekoord wordt geplaatst dat aan een Server van het Beeld moet worden gepubliceerd.

Syntaxis

## Toegestane gebruikerstypen {#section-d670d3af552147199b65c7eb847544a3}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-3580b586296e42a5b21426085b1bb72d}

**Input (createAssetSet)**

<table id="table_2C70C33A127242FC828FCD8EC852E1EC"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Naam </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Vereist </th> 
   <th colname="col4" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> De handgreep naar het bedrijf dat de set activa zal bevatten. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> De handgreep naar de map waarin de nieuwe elementenset wordt gemaakt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Elementnaam. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> subType  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Een unieke id die door de client is gemaakt voor het type elementenset. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setDefinition  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks  </span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> De parameters in de reeks definitiereeks. <p>Deze moeten worden omgezet in de indeling die is opgegeven door de doelviewer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbAssetHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks  </span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> Handgreep van het element dat fungeert als miniatuur voor de nieuwe afbeeldingsset. Als gespecificeerd niet, probeert IPS om het eerste beeldmiddel te gebruiken dat door de reeks van verwijzingen wordt voorzien. </td> 
  </tr> 
 </tbody> 
</table>

**Vervangende functies voor setDefinition**

U kunt vervangende functies op regel opgeven die worden opgelost tijdens het opzoeken of publiceren van een catalogus. Vervangende tekenreeksen hebben de notatie `${<substitution_func>}`. Beschikbare functies worden hieronder opgesomd.

>[!NOTE]
>
>De handvatliterals in parameterlijsten moeten door haakjes `([])` worden omringd. Alle tekst die zich buiten een vervangende tekenreeks bevindt, wordt tijdens de resolutie letterlijk naar de uitvoertekenreeks gekopieerd.

| **Vervangende functie** | **Retourneert** |
|---|---|
| `getFilePath([asset_handle>])` | Het primaire bronbestandspad van het element. |
| `getCatalogId([<asset_handle>])` | De catalogus-id van het element. |
| `getMetaData([<asset_handle>], [<metadata_field_handle>])` | Metagegevenswaarden voor het element. |
| `getThumbCatalogId([<asset_handle>])` | De catalogus-id van het element (alleen voor op afbeeldingen gebaseerde elementen). De catalogus-id van het bijbehorende blokelement (voor andere elementen). Als een gekoppeld blokelement niet beschikbaar is, retourneert de functie een lege tekenreeks. |

**Sample Media setDefinition String**

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])};1,${getFilePath([a|103 
6|19|144])};${getCatalogId([a|452|1|433])};2;${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])} 
```

Tijdens het opzoeken of publiceren van een catalogus wordt dit omgezet in een tekenreeks die lijkt op het volgende:

```java
jcompany/myRenderSet;jcompany/myRenderSet;1,jcompany/Videos/Somebodys_N08275_flv.flv;jcomp any/myimg-1;2;20090703 10:05:53
```

**Uitvoer (createAssetSet)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | Ja | De greep naar de set elementen. |

## Voorbeelden {#section-fed53089de824d67ab96cd9103d384b4}

**Verzoek**

```java
<createAssetSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <companyHandle>c|1</companyHandle> 
   <folderHandle>f|jcompany/AssetSets/</folderHandle> 
   <name>testAssetSet</name> 
   <subType>MediaSet</subType> 
</createAssetSetParam>
```

**Antwoord**

```java
<createAssetSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <assetHandle>a|1801|44|1801</assetHandle> 
</createAssetSetReturn>
```

