---
description: Voeg ruis toe. Hiermee voegt u willekeurige ruis toe aan de voorgrondafbeeldingsgegevens of aan de voorgrond van een effectlaag.
seo-description: Voeg ruis toe. Hiermee voegt u willekeurige ruis toe aan de voorgrondafbeeldingsgegevens of aan de voorgrond van een effectlaag.
seo-title: op_ruis
solution: Experience Manager
title: op_ruis
topic: Scene7 Image Serving - Image Rendering API
uuid: 531f7a94-149b-4090-a163-a1895156250b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# op_ruis{#op-noise}

Voeg ruis toe. Hiermee voegt u willekeurige ruis toe aan de voorgrondafbeeldingsgegevens of aan de voorgrond van een effectlaag.

`op_noise= *``*[,uniform|gaussian[, *`valmonochroom`*]]`

<table id="table_40675464E5824D52BF392ECCE2DDC03C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> val</span> </p> </td> 
   <td colname="col2"> <p>Hoeveelheid ruis in procenten (0...100 int). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> uniform</span> </p> </td> 
   <td colname="col2"> <p>Selecteer uniforme ruisdistributie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> gaussiaans</span> </p> </td> 
   <td colname="col2"> <p>Selecteer Gaussiaanse ruisdistributie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> monochroom</span> </p> </td> 
   <td colname="col2"> <p>Ingesteld op 0 voor kleurruis, 1 voor grijsruis. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`monochrome`* wordt genegeerd voor grijswaardenafbeeldingen.

## Eigenschappen {#section-1f1a64c791f545a3bf1abd0b0e575d87}

Laag, opdracht. Is van toepassing op de huidige laag of op de samengestelde afbeelding, indien van toepassing `layer=comp`.

## Standaard {#section-d548868fa4b64a60bcb481cad1f8113e}

`op_noise=0,uniform,0`, voor geen ruis.
