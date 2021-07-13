---
description: Een materiaal wordt beschouwd als een wandrand wanneer deze is opgegeven in een MSS-wandrand (geïntroduceerd met sub=3.5).
solution: Experience Manager
title: Muurgrenzen
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: e11c38d0-8255-4363-ae60-f47be37a1495
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---

# Muurgrenzen{#wall-borders}

Een materiaal wordt beschouwd als een wandrand wanneer deze is opgegeven in een MSS-wandrand (geïntroduceerd met sub=3.5).

Structuurafbeeldingen met een wandrand kunnen een alfakanaal bevatten om de vorm van de rand te definiëren. De randen van de muur kunnen slechts op wandvoorwerpen worden toegepast.

<table id="table_906C5CC4CADF4024AA0E29544AF48080"> 
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
   <td colname="col3"> <p>Geen </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Resolutie van structuur </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> kenmerk:Resolution  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> anchor=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Horizontale structuuruitlijning (y-waarde wordt genegeerd) </p> </td> 
   <td colname="col3"> <p>0 (linkerrand afbeelding) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> shar=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Verscherpen </p> </td> 
   <td colname="col3"> <p>0 (geen verscherping) </p> </td> 
  </tr> 
 </tbody> 
</table>
