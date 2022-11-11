---
description: Filters die u helpen zoekcriteria te definiëren om zoekopdrachten efficiënter te maken.
solution: Experience Manager
title: SearchFilter
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b3a26966-33c9-48ca-b0ed-d05fc0e2050f
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---

# [!DNL SearchFilter]{#searchfilter}

Filters die u helpen zoekcriteria te definiëren om zoekopdrachten efficiënter te maken.

Syntaxis

## Parameters {#section-4c611d9bbe0d418d882632605fc4d29d}

<table id="table_57CEE262A33A4E898C6AFB30C93FD874"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Naam </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> map</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Geef de map op waarnaar u wilt zoeken. Leeg laten om te zoeken in het hele bedrijf. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolders</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3">Instellen op: 
    <ul id="ul_BD8686943BD14D05A21C00192D4D70D3"> 
     <li id="li_B6A6DE5AAEFF4A80A8413B4785A88222"><span class="codeph"> Waar</span>: De benoemde map en alle submappen doorzoeken. </li> 
     <li id="li_10A581F98B4847ED8EBE4AECC3AD70A8"><span class="codeph"> Onwaar</span>: Alleen de benoemde map zoeken. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:StringArray</span> </td> 
   <td colname="col3">Een lijst met elementtypen die u in een zoekopdracht wilt retourneren. Bijvoorbeeld: <span class="codeph"> image</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:StringArray</span> </td> 
   <td colname="col3"> Geef een elementtype op dat u wilt uitsluiten van een zoekopdracht. Bijvoorbeeld afbeelding. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:StringArray</span> </td> 
   <td colname="col3">Een lijst met subtypen van elementen die u in een zoekopdracht wilt retourneren. Bijvoorbeeld voor een <span class="codeph"> AssetSet</span>, kunt u zoeken naar de <span class="codeph"> MediaType</span> subtype. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> strictSubTypeCheck</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3"> <p>Een optionele booleaanse markering die aangeeft of elementen zonder subtype moeten worden geretourneerd wanneer <span class="codeph"> assetSubTypeArray</span> wordt doorgegeven. </p> <p>Indien waar (true), worden alleen elementen met een van de opgegeven subtypen geretourneerd. </p> <p>Indien false, worden ook elementen zonder subtype geretourneerd. </p> <p>Standaardwaarden zijn false. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeByproducts</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:Boolean</span> </td> 
   <td colname="col3">Instellen op: 
    <ul id="ul_8C164A5D9F0F43968C86A67FA6884F35"> 
     <li id="li_D8009688FF2C439D98D6C1052C1A6CBE"><span class="codeph"> Waar</span>: Alleen oorspronkelijke elementen retourneren. </li> 
     <li id="li_4970226BF0FF42388CAE4415FB63AF16"><span class="codeph"> Onwaar</span>: Om gegenereerde inhoud te retourneren. Bijvoorbeeld afbeeldingen van een geüploade PDF. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3"> Handgreep aan het project u wilt zoeken. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3">Opgeven: 
    <ul id="ul_96FFEE28F7624C1FB0356776B4C7CD53"> 
     <li id="li_DCB07288E5F44E05A4D83D3F34B0E08E"><span class="codeph"> MarkedForPublish</span> alleen gepubliceerde activa retourneren. </li> 
     <li id="li_9A9A852248DB490DB958AE986DF02672"><span class="codeph"> NotMarkedForPublish</span> om alleen niet-gepubliceerde elementen te retourneren. </li> 
    </ul> <p>Opmerking: Leeg laten om te zoeken naar <i>alles</i> gepubliceerde statustypen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> prullenbakState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:tekenreeks</span> </td> 
   <td colname="col3">Opgeven: 
    <ul id="ul_D31B903FA8DA4CFFABAFABA3D8DA91EC"> 
     <li id="li_E4386C8260E64F0BAFE5BA57FF788E48"><span class="codeph"> Alle</span> om elementen te retourneren ongeacht de status van de prullenbak. </li> 
     <li id="li_0B8933FE18C643828075EC8CE8C0223C"><span class="codeph"> NotInTrash</span> om "normale" activa te retourneren. </li> 
     <li id="li_A1F46A0762FA4D4BA9F7247338238DC6"><span class="codeph"> InTrash</span> om elementen uit de prullenbak te retourneren. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>
