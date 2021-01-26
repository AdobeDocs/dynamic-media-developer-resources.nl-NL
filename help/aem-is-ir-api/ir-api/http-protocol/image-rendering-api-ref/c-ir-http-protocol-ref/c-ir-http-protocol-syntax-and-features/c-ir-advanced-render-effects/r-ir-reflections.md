---
description: Vignetten kunnen worden ontworpen om gegevens van de bijna 3D-reflectie op te nemen.
seo-description: Vignetten kunnen worden ontworpen om gegevens van de bijna 3D-reflectie op te nemen.
seo-title: Reflecties
solution: Experience Manager
title: Reflecties
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 6d86f566-0f02-4304-8a6c-08b1a2e9c72e
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---


# Reflecties{#reflections}

Vignetten kunnen worden ontworpen om gegevens van de bijna 3D-reflectie op te nemen.

Indien dit is ontworpen, worden de volgende materiaalkenmerken gebruikt om de reflecterende oppervlakteigenschappen van het materiaal te definiëren:

<table id="table_8769C726A17E412FB41F7CB87690B1FE"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Kenmerk </p> </th> 
   <th class="entry"> <p>Beschrijving </p> </th> 
   <th class="entry"> <p>Standaard </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca" type="reference" format="dita" scope="local"> <span class="codeph"> gloss=</span> </a> </p> </td> 
   <td> <p>Oppervlakglans </p> </td> 
   <td> <p>Van vignet </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a" type="reference" format="dita" scope="local"> <span class="codeph"> glossmap=  </span> </a> </p> </td> 
   <td> <p>Glansvariatie (grijswaardenafbeelding) </p> </td> 
   <td> <p>Geen </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180" type="reference" format="dita" scope="local"> <span class="codeph"> hard=  </span> </a> </p> </td> 
   <td> <p>Oppervlakteruwheid </p> </td> 
   <td> <p>40% </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35" type="reference" format="dita" scope="local"> <span class="codeph"> type=</span> </a> </p> </td> 
   <td> <p>Materiaaltype </p> </td> 
   <td> <p>0 (onbekend) </p> </td> 
  </tr> 
 </tbody> 
</table>

De renderer past het bereik van het kenmerk `gloss=` en `rough=` aan volgens `type=`. Sommige materiaaltypen zoals stof zijn over het algemeen minder reflectief dan materiaaltypen zoals steen of metaal, en dezelfde hoeveelheid glansstof die voor een van deze typen is opgegeven, resulteert in een ander reflectie-effect dan het andere. `gloss=`en ruwheid hebben een vrij brede kleuromvang als niet gespecificeerd  `type=` is of aan 0 wordt geplaatst.

`glossmap=` kan worden gebruikt om de glans van een materiaal per pixel te bepalen.
