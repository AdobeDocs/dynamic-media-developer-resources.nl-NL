---
description: Hiermee kunt u uitsnijden naar het selectiekader van een ingesloten pad met een naam. Door deze uitsnijding wordt de grootte van de afbeelding gewijzigd.
solution: Experience Manager
title: cropPathE
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 78e9f994-d638-49a7-ac42-3146e47210e3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---

# cropPathE{#croppathe}

Hiermee kunt u uitsnijden naar het selectiekader van een ingesloten pad met een naam. Door deze uitsnijding wordt de grootte van de afbeelding gewijzigd.

`cropPathE= *`pathName`*&#42;[, *`pathName`*]`

<table id="table_598304852E844456AB3AC9FF1F178B71"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pathName</span></span> </p> </td> 
   <td colname="col2"> <p>Naam van pad dat is ingesloten in bronafbeelding van laag (alleen ASCII). </p> <p> <span class="codeph"><span class="varname"> pathName</span></span> Dit is de naam van een pad dat is ingesloten in de bronafbeelding van de laag. Het pad wordt zo nodig automatisch getransformeerd om relatieve uitlijning met de inhoud van de afbeelding te behouden. Indien meer dan één <span class="codeph"><span class="varname"> pathName</span></span> wordt opgegeven, wordt de server één voor één uitgesneden op het selectiekader van elk pad. Alle <span class="codeph"><span class="varname"> pathName</span></span> niet gevonden in de bronafbeelding wordt genegeerd. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

Laagkenmerk. Is van toepassing op de huidige laag of op de samengestelde afbeelding als `layer=comp`. Genegeerd door effectlagen.

`cropPathE=` wordt genegeerd als er geen pad met de opgegeven naam is gevonden in de bronafbeelding van de laag of als de laagbron geen afbeelding is.

## Standaard {#section-d1986aa31af14767aeb1b4a57add67f4}

Geen, voor geen extra uitsnijding van de laag.

## Zie ook {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[uitsnijden](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab), [clipPathE](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
