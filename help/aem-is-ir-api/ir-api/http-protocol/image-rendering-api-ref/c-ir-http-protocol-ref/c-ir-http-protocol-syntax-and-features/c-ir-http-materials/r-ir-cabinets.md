---
description: De materialen van kabinetten specificeren een dossier van het kabinetsstijl (.vnc- dossieruitbreiding), een speciaal gegevensdossier dat fotografische vertegenwoordiging van kabinetten samen met parametrische lay-outdefinities en andere informatie vereist voor het teruggeven van kabinetsfronten bevat.
seo-description: De materialen van kabinetten specificeren een dossier van het kabinetsstijl (.vnc- dossieruitbreiding), een speciaal gegevensdossier dat fotografische vertegenwoordiging van kabinetten samen met parametrische lay-outdefinities en andere informatie vereist voor het teruggeven van kabinetsfronten bevat.
seo-title: Cabinetten
solution: Experience Manager
title: Cabinetten
topic: Scene7 Image Serving - Image Rendering API
uuid: d515c613-07c5-49ef-ad6e-568a1f6c1335
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 0%

---


# Cabinetten{#cabinets}

De materialen van kabinetten specificeren een dossier van het kabinetsstijl (.vnc- dossieruitbreiding), een speciaal gegevensdossier dat fotografische vertegenwoordiging van kabinetten samen met parametrische lay-outdefinities en andere informatie vereist voor het teruggeven van kabinetsfronten bevat.

[!DNL vnc] bestanden kunnen een herhaalbare houten korrelstructuur bevatten of de structuur kan extern via een tweede argument worden opgegeven  `src=`. Met bepaalde [!DNL vnc]-bestanden kunt u geselecteerde gebieden met kabinetsvoorvoegsels vullen met kleur of structuur (doorgaans gebruikt voor laminaatkaststijlen).

Cabinematerialen kunnen alleen op kabinetsobjecten worden toegepast.

<table id="table_0B16200886FE4DFEBB1E4BE8FBA67EE4"> 
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
   <td colname="col2"> <p>bestand in kabinetstijl; vereist. </p> </td> 
   <td colname="col3"> <p>Geen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Optioneel afbeeldingsbestand met structuur (tweede waarde voor <span class="codeph"> src= </span>). </p> </td> 
   <td colname="col3"> <p>Geen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Optionele structuurresolutie. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> kenmerk:Resolution  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph"> color=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Hiermee kleurt u de kast en/of structuur. </p> </td> 
   <td colname="col3"> <p>Geen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> shar=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Verscherpen. </p> </td> 
   <td colname="col3"> <p>0 (geen verscherping) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-flags.md#reference-3a4844f0f21346d79e6508aaad9a9ac9" type="reference" format="dita" scope="local"> <span class="codeph"> flags=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Speciale rendermarkeringen. </p> </td> 
   <td colname="col3"> <p>0 (geen markeringen) </p> </td> 
  </tr> 
 </tbody> 
</table>

