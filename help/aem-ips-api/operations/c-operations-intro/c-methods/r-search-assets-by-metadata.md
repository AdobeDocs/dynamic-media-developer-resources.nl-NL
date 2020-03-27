---
description: Zoekt de gegevensopslagplaats van de meta-gegevensindex naar de bepaalde onderzoekstermijnen. Retourneert elementgegevens zoals de methode searchAssets.
seo-description: Zoekt de gegevensopslagplaats van de meta-gegevensindex naar de bepaalde onderzoekstermijnen. Retourneert elementgegevens zoals de methode searchAssets.
seo-title: searchAssetsByMetadata
solution: Experience Manager
title: searchAssetsByMetadata
topic: Scene7 Image Production System API
uuid: f4119ee9-f6d8-49fb-9d8c-bb200951d983
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# searchAssetsByMetadata{#searchassetsbymetadata}

Zoekt de gegevensopslagplaats van de meta-gegevensindex naar de bepaalde onderzoekstermijnen. Retourneert elementgegevens zoals de methode searchAssets.

Hoewel `searchAssetsByMetadata` u kunt zoeken op door de gebruiker gedefinieerde metagegevensvelden, worden deze velden niet geretourneerd als ze zijn opgegeven in het `responseMetadataArray`bestand. Ter illustratie dit punt, het volgende codevoorbeeld:

```java
<ns:responseMetadataArray>
 <ns:items>custom_attributes.x</ns:items>
</ns:responseMetadataArray>
```

retourneert een null-waarde:

```java
<items>
 <name>custom_attributes.x</name>
 <value>null</value>
</items>
```

U kunt dit probleem omzeilen door de elementen te gebruiken die door de zoekopdracht worden geretourneerd `fieldHandles` (zie ook `getAssets` getAssets [](../../../operations/c-operations-intro/c-methods/r-get-assets.md#reference-adad4f504f684d3dabc09e093b8511ca)). Deze methode krijgt de Gebruiker - bepaalde waarden van Gebieden voor de activa in kwestie. Gebruik het volgende syntaxisvoorbeeld aan onderzoek tegen user-defined Gebieden van Meta-gegevens:

```java
<ns:metadataConditionArray>
 <ns:items>
  <ns:fieldHandle>custom_attributes.[UDF Field Name]</ns:fieldHandle>
  <ns:op>[Conditional]</ns:op>
  <ns:value>[Value]</ns:value>
 </ns:items>
</ns:metadataConditionArray>
```

## Geautoriseerde gebruikerstypen {#section-9f85dd55ab574104b5fdc0f95aa0a0e2}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-5f1edb9c5b914160ab361f4364b8aa8d}

**Input (searchAssetsByMetadataParam)**

<table id="table_8FF228D6279241849F3D9E5BA080580C"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> bedrijfshandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:tekenreeks</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>De handgreep aan het bedrijf. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> Filter</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> tekst:SearchFilter</span> </p> </td> 
   <td colname="col3"> <p>Nee </p> </td> 
   <td colname="col4"> <p>Filters die u helpen zoekcriteria te definiëren. </p> <p>Zie <a href="../../../types/c-data-types/r-search-filter.md#reference-0e2eb87bccae4b69be6717267bcb80aa" format="dita" scope="local"> Zoekfilter</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> metadataConditionArray</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> type:MetadataConditionArray</span> </p> </td> 
   <td colname="col3"> <p>Nee </p> </td> 
   <td colname="col4"> <p>Voorwaarden die zoekcriteria definiëren. Zie hieronder voor meer informatie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> responseMetadataArray</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> type:StringArray</span> </p> </td> 
   <td colname="col3"> <p>Nee </p> </td> 
   <td colname="col4"> <p>De extra gebieden u op de reactie in het activaoverzicht wilt bevolken. De velden moeten in de genormaliseerde indeling worden opgegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> recordsPerPage</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>Nee </p> </td> 
   <td colname="col4"> <p>Het aantal elementen dat door de reactie wordt geretourneerd. De standaardwaarde is 1000. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> resultPage</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>Nee </p> </td> 
   <td colname="col4"> <p>Hiermee geeft u de resultatenpagina op die u wilt retourneren, op basis van het paginaformaat <span class="codeph"> recordsPerPage</span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Sorteren op</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:tekenreeks</span> </p> </td> 
   <td colname="col3"> <p>Nee </p> </td> 
   <td colname="col4"> <p>Sorteren op geselecteerd elementveld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> sorteerrichting</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:tekenreeks</span> </p> </td> 
   <td colname="col3"> <p>Nee </p> </td> 
   <td colname="col4"> <p>Keuze van sorteerrichting. Oplopend is standaard. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (searchAssetsByMetadataReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`totalRows`*` | `xsd:int` | Nee | Aantal overeenkomsten. |
| ` *`assetArray`*` | `types:AssetArray` | Nee | Array met elementen die door de zoekopdracht worden geretourneerd. |

## details metadataConditionArray {#section-1af4a4a22f82451eabdf6dfe13d9f27d}

**Itemstructuur**

`metadataConditionArray` de structuur is als volgt:

```java
<ns1:items>
   <ns:fieldHandle>field_handle</ns:fieldHandle>
   <ns:op>operator</ns:op>
   <ns:value>comparison_value</ns:value>
</ms1:items>
```

**Waarden**

`field_handle` is de zoeksleutel voor metagegevens. Het kan puntnotatie bevatten. Mogelijke waarden zijn:

* `asset_id` (zonder voorvoegsel)
* `name`
* `folder_path`
* `type`
* `file_name`
* `description`
* `comment`
* `user_data`
* `sku`
* `modified_at`
* `modified_by`
* `created_at` (zelfde als `modified_at` (Datum in de vorm: 25 juli 2014 22:13:45 GMT-0500 (CDT)

* `created_by`

**Toegestane operatoren**

In dit hoofdstuk [!DNL operator] wordt gedefinieerd hoe de waarde moet worden vergeleken en opgenomen:

* `Equals`
* `NotEquals`
* `Contains`
* `NotContains`
* `StartsWith`
* `EndsWith`

Het `comparison_value` is de term die u zoekt.

## Voorbeelden {#section-53a12b9c023e4e629eddf5719c955ad4}

In dit codevoorbeeld wordt gezocht met de volgende metagegevenscriteria:

* `name` bevat `1000801`.

* `dc.rights` veld is gelijk aan `Per Jessen Schmidt`.

**Verzoek**

```java
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:xsd="http://www.scene7.com/IpsApi/xsd"
xmlns:ns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <soapenv:Header>
      <xsd:authHeader>
          <xsd:user>user@adobe.com</xsd:user>
          <xsd:password>topSecret</xsd:password>
      </xsd:authHeader>
   </soapenv:Header>
   <soapenv:Body>
      <ns:searchAssetsByMetadataParam>
         <ns:companyHandle>c|656</ns:companyHandle>
         <ns:metadataConditionArray>
            <ns:items>
               <ns:fieldHandle>name</ns:fieldHandle>
               <ns:op>Contains</ns:op>
               <ns:value>1000801</ns:value>
            </ns:items>
            <ns:items>
               <ns:fieldHandle>dc.rights</ns:fieldHandle>
               <ns:op>Equals</ns:op>
               <ns:value>Per Jessen Schmidt</ns:value>
            </ns:items>
         </ns:metadataConditionArray>
         <ns:responseMetadataArray>
            <ns:items>dc.subject</ns:items>
            <ns:items>xmp.CreatorTool</ns:items>
         </ns:responseMetadataArray>
      </ns:searchAssetsByMetadataParam>
   </soapenv:Body>
</soapenv:Envelope>
```

**Antwoord**

```java
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/">
   <soapenv:Body>
      <searchAssetsByMetadataReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
         <totalRows>1</totalRows>
         <assetSummaryArray>
            <items>
               <assetHandle>a|885289</assetHandle>
               <type>Image</type>
               <name>test9-1000801</name>
               <folder>Extroscope/Test subfolders/</folder>
               <filename>test9-1000801.jpg</filename>
               <created>2009-11-19T07:21:24.252-08:00</created>
               <createUser>pschmidt@adobe.com</createUser>
               <lastModified>2009-11-19T07:21:25.487-08:00</lastModified>
               <lastModifyUser>pschmidt@adobe.com</lastModifyUser>
               <metadataArray>
                  <items>
                     <name>dc.subject</name>
                     <value>[San Fransico, USA</value>
                  </items>
                  <items>
                     <name>xmp.CreatorTool</name>
                     <value>Ver.1.0</value>
                  </items>
               </metadataArray>
            </items>
         </assetSummaryArray>
      </searchAssetsByMetadataReturn>
   </soapenv:Body>
</soapenv:Envelope>
```

