---
description: Verwijdert metagegevenswaarden voor een element. Werkt met een array van metagegevens verwijderen om waarden in een batch in te stellen.
seo-description: Verwijdert metagegevenswaarden voor een element. Werkt met een array van metagegevens verwijderen om waarden in een batch in te stellen.
seo-title: deleteAssetMetadata
solution: Experience Manager
title: deleteAssetMetadata
topic: Scene7 Image Production System API
uuid: 2dc783c6-23da-4a94-8780-3c4ec88ff3f4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---


# deleteAssetMetadata{#deleteassetmetadata}

Verwijdert metagegevenswaarden voor een element. Werkt met een array van metagegevens verwijderen om waarden in een batch in te stellen.

Syntaxis

## Toegestane gebruikerstypen {#section-e913be43b684491daf02bc73211e4290}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>De gebruiker moet lees- en verwijdertoegang tot het element hebben.

## Parameters {#section-0eed164e278b456fbdfb7a50727a0416}

**Input (deleteAssetMetadataParam)**

<table id="table_A4438E2FE5F245E5B73F46CD887BE70F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Naam </p> </th> 
   <th colname="col2" class="entry"> <p>Type </p> </th> 
   <th colname="col3" class="entry"> <p>Vereist </p> </th> 
   <th colname="col4" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>companyHandle </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:tekenreeks</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>De handgreep van het bedrijf waartoe de map behoort. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>assetHandle </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:tekenreeks</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>De handgreep van het element dat moet worden verwijderd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>metadataDelete </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:tekenreeks</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Metagegevens die uit het element moeten worden verwijderd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>deleteArray </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:MetadataDeleteArray</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Array met metagegevens die uit het element moeten worden verwijderd. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (deleteAssetMetadataParam)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-d5657289f5234bb0a613dcf691507958}

MetadataDelete

```java
    <complexType name="MetadataDelete">
        <sequence>
            <element name="fieldHandle" type="xsd:string"/>
        </sequence>
    </complexType>
```

Voorbeeldaanroep

```java
<ac:Request id="deleteAssetMetadata">
 <deleteAssetMetadataParam xmlns="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
  <companyHandle>c|101</companyHandle>
  <assetHandle>a|202</assetHandle>
  <deleteArray>
   <items>
    <fieldHandle>m|2919|ASSET|UntypedUDFField1395788289789</fieldHandle>
   </items>
  </deleteArray>
 </deleteAssetMetadataParam>
</ac:Request>
```

