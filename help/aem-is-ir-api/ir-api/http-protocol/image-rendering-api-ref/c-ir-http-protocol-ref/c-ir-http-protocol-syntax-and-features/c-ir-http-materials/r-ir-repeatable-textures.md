---
description: Herhalbare structuren omvatten materialen van binnen- en buitenkant, zoals weefsels (zowel kleding als bekleding), vloer-wandbekledingen, wandpapier, tegenwerpmaterialen, houten korrelstructuren, dakbedekking en lijfmaterialen, en alle andere generieke structuren.
seo-description: Herhalbare structuren omvatten materialen van binnen- en buitenkant, zoals weefsels (zowel kleding als bekleding), vloer-wandbekledingen, wandpapier, tegenwerpmaterialen, houten korrelstructuren, dakbedekking en lijfmaterialen, en alle andere generieke structuren.
seo-title: Herhaalbare structuren
solution: Experience Manager
title: Herhaalbare structuren
topic: Scene7 Image Serving - Image Rendering API
uuid: 11a55d9f-a1d7-490e-af0e-9bf2c3a35501
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---


# Herhalbare structuren{#repeatable-textures}

Herhalbare structuren omvatten materialen van binnen- en buitenkant, zoals weefsels (zowel kleding als bekleding), vloer-wandbekledingen, wandpapier, tegenwerpmaterialen, houten korrelstructuren, dakbedekking en lijfmaterialen, en alle andere generieke structuren.

Herhalbare structuren kunnen worden toegepast op vlakke, stroomlijnobjecten, schetsen-, vlak-, wand- en kabinetsobjecten. Wanneer het object wordt toegepast op een niet-tekentabel object, wordt het object getekend met `color=` (of `bgc=` als `color=` niet is opgegeven).

Een materiaal wordt beschouwd als een structuur als het een `src=`-kenmerk bevat dat een afbeelding opgeeft en als het voorkomt in een ander MSS dan een andere rand dan een decal- of wandrand.

Bij het renderen wordt de structuur uitgelijnd met het object door het `anchor=`-punt van het structuurmateriaal te laten overeenkomen met het oorsprongpunt van de structuur van het object (zoals in het vignet is geschreven).

<table id="table_992A6E93E4274B598A236F8F728F017A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Kenmerk </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
   <th colname="col3" class="entry"> <p>Standaard </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Herhalbare structuurafbeelding; vereist </p> </td> 
   <td colname="col3"> <p>Geen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Resolutie van structuur </p> </td> 
   <td colname="col3"> <span class="codeph"> kenmerk:Resolution  </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> anchor=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Uitlijningspunt van structuur </p> </td> 
   <td colname="col3"> <p>Linkerbovenhoek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> repeat=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Herhalingsmodus </p> </td> 
   <td colname="col3"> <p>0 (recht herhalen). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> shar=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Verscherpen </p> </td> 
   <td colname="col3"> <p>0 (geen verscherping). </p> </td> 
  </tr> 
 </tbody> 
</table>

Naast deze basiskenmerken ondersteunen herhaalbare structuren de volgende speciale kenmerken voor geavanceerde toepassingen:

<table id="table_A97365804CB143DEB31F26A65DA3CE04"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Kenmerk </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
   <th colname="col3" class="entry"> <p>Standaard </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a" type="reference" format="dita" scope="local"> <span class="codeph"> grot=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Gegroepeerde kleur en dikte; nuttig voor keramische/steenkool </p> </td> 
   <td colname="col3"> <p>Groepering al aanwezig in afbeelding </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7" type="reference" format="dita" scope="local"> <span class="codeph"> align=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Uitlijningsmodus (tussen objecten); gebruikt voor upholstertoepassingen </p> </td> 
   <td colname="col3"> <p>Gecentreerd </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rotate.md#reference-3745d74a913e4065b7ac009fb4fd9e3c" type="reference" format="dita" scope="local"> <span class="codeph"> roteren=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Rotatiehoek structuur; niet ondersteund door wandobjecten </p> </td> 
   <td colname="col3"> <p>0 (geen rotatie) </p> </td> 
  </tr> 
 </tbody> 
</table>

