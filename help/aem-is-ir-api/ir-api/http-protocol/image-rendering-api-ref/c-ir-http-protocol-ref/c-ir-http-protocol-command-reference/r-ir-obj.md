---
description: Selecteer object op naam. Hiermee wordt de opgegeven groep vignetten op naam geselecteerd en wordt een nieuw MSS gestart.
seo-description: Selecteer object op naam. Hiermee wordt de opgegeven groep vignetten op naam geselecteerd en wordt een nieuw MSS gestart.
seo-title: obj
solution: Experience Manager
title: obj
topic: Scene7 Image Serving - Image Rendering API
uuid: 2fede992-6759-45bd-b2f1-36e2c791d536
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 0%

---


# obj{#obj}

Selecteer object op naam. Hiermee wordt de opgegeven groep vignetten op naam geselecteerd en wordt een nieuw MSS gestart.

` obj= *`name`*`

<table id="simpletable_6E0DA6CBCDCF4CDDAFA5A4C38E0D5FC5"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name  </span> </span> </p> </td> 
  <td class="stentry"> <p>Groepsnaam of pad/naam. </p> </td> 
 </tr> 
</table>

Subgroepen of afzonderlijke objecten kunnen worden geselecteerd met behulp van een volledig gekwalificeerd groepspad (d.w.z. door de naam van de doelgroep of het doelobject op te geven, voorafgegaan door alle bovenliggende groepen, gescheiden door / (slashes).

Wanneer geen groep/object met de opgegeven naam wordt gevonden, wordt de in `attribute::OnObjFail` opgegeven handeling uitgevoerd.

## Eigenschappen {#section-9463b36e8ff74c81a70c7c2b58927430}

Selectieopdracht; MSS-scheidingsteken. De objectselectie is blijvend totdat een ander object is geselecteerd, met `obj=` of `sel=`.

Paden en namen van groepen/objecten zijn niet hoofdlettergevoelig.

## Standaard {#section-0c322850512c4896bb551856a549440e}

De eerste groep in het vignet die renderbare objecten bevat, wordt automatisch geselecteerd wanneer een nieuw vignet wordt geopend.

## Zie ook {#section-d9d2c92ef48548f48b9781e2a8a5fb5a}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b),  [kenmerk::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
