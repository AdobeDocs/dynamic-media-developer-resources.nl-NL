---
description: Maak een nieuwe afbeeldingskaart of bewerk een bestaande kaart.
seo-description: Maak een nieuwe afbeeldingskaart of bewerk een bestaande kaart.
seo-title: saveImageMap
solution: Experience Manager
title: saveImageMap
topic: Scene7 Image Production System API
uuid: 9714fc99-2259-4766-96d7-fe2f9fd2f341
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 0%

---


# saveImageMap{#saveimagemap}

Maak een nieuwe afbeeldingskaart of bewerk een bestaande kaart.

Syntaxis

## Toegestane gebruikerstypen {#section-9ef194a67b3546fb82ed7bb294bc2714}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>De gebruiker moet lees- en schrijftoegang tot het element hebben.

## Parameters {#section-64f7f5fd8f954fba9fa30eeee556863a}

**Input (saveImageMapParam)**

<table id="table_49649036F46941D2B1F28515674E533B"> 
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
   <td colname="col4"> De handgreep van het bedrijf met de afbeeldingskaart die u wilt opslaan. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> De handgreep van het afbeeldingselement waartoe de afbeelding met hyperlinks behoort. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageMapHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks  </span> </td> 
   <td colname="col3"> Nee </td> 
   <td colname="col4"> De handgreep van de afbeelding met hyperlinks. Maakt een afbeelding met hyperlinks als deze NULL is. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> De naam van de afbeeldingskaart die is gemaakt of opgeslagen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> shapeType  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Keuze van regiovorm. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> regio  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Een door komma's gescheiden lijst met punten die het gebied definiëren. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> action  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> <p>De <span class="codeph"> href </span> waarde verbonden aan de beeldkaart zoals gespecificeerd in de IPS interface. </p> <p>Om de <span class="codeph"> href </span> waarde te verkrijgen, klik het beeld in de IPS interface, kopieer en plak URL in dit element, en formatteer dan IPS URL als juiste URL. <span class="codeph"> &amp; </span> wordt bijvoorbeeld <span class="codeph"> &amp;amp; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> positie  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> De volgorde in de lijst met afbeeldingen met hyperlinks (de Z-as). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> enabled  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean  </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"></td> 
  </tr> 
 </tbody> 
</table>

**Output (saveImageMapReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`imageMapHandle`*` | `xsd:string` | Ja | De handgreep van de nieuwe of bewerkte afbeelding met hyperlinks. |

## Voorbeelden {#section-fdac488b640f427c8aa3d549c5032851}

In dit codevoorbeeld wordt een nieuwe afbeeldingskaart voor een element gemaakt. Er wordt een vormtype gebruikt dat wordt bepaald door een tekenreeksconstante voor de vorm van het gebied en er wordt een handgreep geretourneerd naar de nieuwe afbeeldingskaart.

**Verzoek**

```
<saveImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <companyHandle>47</companyHandle> 
   <assetHandle>24266|1|17062</assetHandle> 
   <name>My Image Map</name> 
   <shapeType>Rectangle</shapeType> 
   <region>0,10,0,10</region> 
   <action>http://s7oslo.macromedia.com/scene7/browse/MoreInfo.jsp?assetID=24266&amp; 
   iRow=1&iRows=1&amp;strSearchType=image</action> 
   <position>0</position> 
</saveImageMapParam>
```

**Antwoord**

```
<saveImageMapReturn xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <imageMapHandle>34191|8|554</imageMapHandle> 
</saveImageMapReturn>
```

