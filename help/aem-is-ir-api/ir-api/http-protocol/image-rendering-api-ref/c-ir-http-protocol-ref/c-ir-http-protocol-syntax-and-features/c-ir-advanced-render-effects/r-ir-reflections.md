---
title: Reflecties
description: Vignetten kunnen worden ontworpen om gegevens van de bijna 3D-reflectie op te nemen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f67ede68-03c0-461f-a16d-a308f76fd24c
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '136'
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
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a" type="reference" format="dita" scope="local"> <span class="codeph"> glossmap= </span> </a> </p> </td> 
   <td> <p>Glansvariatie (grijswaardenafbeelding) </p> </td> 
   <td> <p>Geen </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180" type="reference" format="dita" scope="local"> <span class="codeph"> hard= </span> </a> </p> </td> 
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

De renderer past het bereik van de `gloss=` en `rough=` kenmerk volgens `type=`. Sommige materiaaltypen, zoals weefsels, zijn minder reflecterend dan materiaaltypen zoals steen of metaal. Bovendien leidt dezelfde hoeveelheid glanzen die voor een van deze twee is opgegeven vaak tot een ander reflectie-effect dan voor een ander effect. Het kenmerk `gloss=` en ruwheid hebben een tamelijk brede kleuromvang als `type=` is niet opgegeven of is ingesteld op `0`.

`glossmap=` Wordt gebruikt om de glans van een materiaal per pixel te bepalen.
