---
description: Hiermee kunt u uitsnijden naar het selectiekader van een ingesloten pad met een naam. Door deze uitsnijding wordt de grootte van de afbeelding gewijzigd.
seo-description: Hiermee kunt u uitsnijden naar het selectiekader van een ingesloten pad met een naam. Door deze uitsnijding wordt de grootte van de afbeelding gewijzigd.
seo-title: cropPathE
solution: Experience Manager
title: cropPathE
topic: Scene7 Image Serving - Image Rendering API
uuid: 4689fd20-dfa0-47eb-8184-cd233f1ac088
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# cropPathE{#croppathe}

Hiermee kunt u uitsnijden naar het selectiekader van een ingesloten pad met een naam. Door deze uitsnijding wordt de grootte van de afbeelding gewijzigd.

`cropPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="table_598304852E844456AB3AC9FF1F178B71"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pathName</span></span> </p> </td> 
   <td colname="col2"> <p>Naam van pad dat is ingesloten in bronafbeelding van laag (alleen ASCII). </p> <p> <span class="codeph"><span class="varname"> pathName</span></span> is de naam van een pad dat is ingesloten in de bronafbeelding van de laag. Het pad wordt zo nodig automatisch getransformeerd om relatieve uitlijning met de inhoud van de afbeelding te behouden. Als er meer dan één <span class="codeph"><span class="varname"> pathName</span></span> is opgegeven, snijdt de server één voor één uit naar het selectiekader van elk pad. Eventuele <span class="codeph"><span class="varname"> padnamen</span></span> die niet in de bronafbeelding worden gevonden, worden genegeerd. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

Laagkenmerk. Is van toepassing op de huidige laag of op de samengestelde afbeelding, indien van toepassing `layer=comp`. Genegeerd door effectlagen.

`cropPathE=` wordt genegeerd als er geen pad met de opgegeven naam is gevonden in de bronafbeelding van de laag of als de laagbron geen afbeelding is.

## Standaard {#section-d1986aa31af14767aeb1b4a57add67f4}

Geen, voor geen extra uitsnijding van de laag.

## Zie ook {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[uitsnijden](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab), [clipPathE](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
