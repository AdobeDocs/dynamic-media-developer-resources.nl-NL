---
description: Decal-materialen omvatten kledingconstructies zoals apparaten, T-shirtafdrukken en geborduurde of gedrukte logo's, alsmede niet-herhaalbare, platte objecten die worden gebruikt in toepassingen voor binnen- en buitengebruik, zoals vlakbedekking, wandjagers, borden, enzovoort.
seo-description: Decal-materialen omvatten kledingconstructies zoals apparaten, T-shirtafdrukken en geborduurde of gedrukte logo's, alsmede niet-herhaalbare, platte objecten die worden gebruikt in toepassingen voor binnen- en buitengebruik, zoals vlakbedekking, wandjagers, borden, enzovoort.
seo-title: Decals
solution: Experience Manager
title: Decals
topic: Scene7 Image Serving - Image Rendering API
uuid: 6e64f382-f15f-4018-b00c-4fd21a4ebc8c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Decals{#decals}

Decal-materialen omvatten kledingconstructies zoals apparaten, T-shirtafdrukken en geborduurde of gedrukte logo&#39;s, alsmede niet-herhaalbare, platte objecten die worden gebruikt in toepassingen voor binnen- en buitengebruik, zoals vlakbedekking, wandjagers, borden, enzovoort.

Een materiaal wordt als een decal beschouwd als het in een decal MSS is gespecificeerd. Een decal is doorgaans een RGBA-afbeelding, waarbij het alfakanaal de vorm van het decal definieert.

Er kan één decal worden toegepast op elk vlak, stroomlijn, schets, vlak of wandobject (tenzij de markering Geen structuur is ingesteld). Decals worden toegepast op het object door de decal&#39;s uit te lijnen `anchor=` met het decimale oorsprongpunt van het vignetobject. De positie kan verder worden aangepast met `pos=`.

Een slagschaduw wordt weergegeven als het decale materiaal een dikte definieert en het vignetobject een lichtvector definieert.

<table id="table_3F119BC9B7654FD092826A34F5827268"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Kenmerk </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
   <th colname="col3" class="entry"> <p>Standaard </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span></a> </p> </td> 
   <td colname="col2"> <p>Afbeelding (meestal met alfa); vereist. </p> </td> 
   <td colname="col3"> <p>Geen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988" type="reference" format="dita" scope="local"> <span class="codeph"> size= </span></a> </p> </td> 
   <td colname="col2"> <p>Decale breedte, hoogte en dikte (voor slagschaduw). </p> </td> 
   <td colname="col3"> <p> <span class="varname"> imageWidth </span> x <span class="codeph"> res </span>, <span class="varname"> imageHeight </span> x <span class="codeph"> res, 0 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span></a> </p> </td> 
   <td colname="col2"> <p>Resolutie van structuur (genegeerd als size= is opgegeven). </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> kenmerk:Resolution </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> anchor= </span></a> </p> </td> 
   <td colname="col2"> <p>Decal alignment point. </p> </td> 
   <td colname="col3"> <p>Midden afbeelding. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pos.md#reference-22c10904a0ce4c8bb41c2c78104221b8" type="reference" format="dita" scope="local"> <span class="codeph"> pos= </span></a> </p> </td> 
   <td colname="col2"> <p>Relatieve decimale positie. </p> </td> 
   <td colname="col3"> <p>0, 0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-opac.md#reference-136b8563da714313a9e103f4ce179c5b" type="reference" format="dita" scope="local"> <span class="codeph"> opac= </span></a> </p> </td> 
   <td colname="col2"> <p>Decale dekking. </p> </td> 
   <td colname="col3"> <p>100% </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> scherp= </span></a> </td> 
   <td colname="col2"> <p>Verscherpen. </p> </td> 
   <td colname="col3"> <p>0 (geen verscherping) </p> </td> 
  </tr> 
 </tbody> 
</table>

