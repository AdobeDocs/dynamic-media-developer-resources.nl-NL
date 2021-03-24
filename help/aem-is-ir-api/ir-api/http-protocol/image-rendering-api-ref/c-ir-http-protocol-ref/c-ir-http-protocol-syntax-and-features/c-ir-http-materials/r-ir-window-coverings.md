---
description: Tot vensterbekledingsmaterialen behoren zowel zachte vensterbekledingen (lakens, valanties, cafégordijnen) als harde vensterbekledingen (tinten en jaloezieën).
solution: Experience Manager
title: Vensterbedekkingen
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---


# Vensterbedekkingen{#window-coverings}

Tot vensterbekledingsmaterialen behoren zowel zachte vensterbekledingen (lakens, valanties, cafégordijnen) als harde vensterbekledingen (tinten en jaloezieën).

Met vensterbedekkende materialen geeft u een *venster op dat stijlbestand* ( [!DNL .vnw] bestandsextensie) bedekt, een speciaal gegevensbestand dat lijkt op een vignet, met masker-, belichting-, layout- en structuurgegevens die de vensterbedekking definiëren.

[!DNL vnw] De bestanden bevatten niet de kleur en structuur (stof) voor de vensterbedekking. Deze informatie wordt afzonderlijk opgegeven, net als herhaalbare structuren.

Vensters die materialen bedekken, kunnen alleen worden toegepast op Window Covering Frame Objects, die overlappende objecten zijn.

<table id="table_545865B054E84592BDAEDA57DBFAE9B3"> 
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
   <td colname="col2"> <p>een Window bekleding style file; vereist. </p> </td> 
   <td colname="col3"> <p>Geen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Afbeeldingsbestand van structuur (tweede waarde voor <span class="codeph"> src= </span>). </p> </td> 
   <td colname="col3"> <p>Geen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Resolutie van structuur. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> kenmerk:Resolution  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> repeat=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Herhalingsmodus. </p> </td> 
   <td colname="col3"> <p>0 (recht herhalen) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph"> color=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Effen kleur (of kleurt structuur). </p> </td> 
   <td colname="col3"> <p>128 (neutraal grijs) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> shar=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Verscherpen. </p> </td> 
   <td colname="col3"> <p>0 (geen verscherping) </p> </td> 
  </tr> 
 </tbody> 
</table>

