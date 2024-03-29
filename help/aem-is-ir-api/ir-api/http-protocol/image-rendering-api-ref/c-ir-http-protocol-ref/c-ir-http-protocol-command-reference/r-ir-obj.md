---
title: obj
description: Selecteer object op naam. Hiermee wordt de opgegeven groep vignetten op naam geselecteerd en wordt een nieuw MSS gestart.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 17387203-f7a7-4876-a15b-2084894f981d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---

# obj{#obj}

Selecteer object op naam. Hiermee wordt de opgegeven groep vignetten op naam geselecteerd en wordt een nieuw MSS gestart.

` obj= *`name`*`

<table id="simpletable_6E0DA6CBCDCF4CDDAFA5A4C38E0D5FC5"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name </span> </span> </p> </td> 
  <td class="stentry"> <p>Groepsnaam of pad/naam. </p> </td> 
 </tr> 
</table>

Subgroepen of afzonderlijke objecten kunnen worden geselecteerd met een volledig gekwalificeerd groepspad (dat wil zeggen door de naam van de doelgroep of het doelobject op te geven, voorafgegaan door alle bovenliggende groepen, gescheiden door / (slashes).

Als er geen groep/object met de opgegeven naam wordt gevonden, wordt de handeling opgegeven in `attribute::OnObjFail` wordt genomen.

## Eigenschappen {#section-9463b36e8ff74c81a70c7c2b58927430}

Selectie, opdracht; MSS-scheidingsteken. De objectselectie is blijvend totdat een ander object is geselecteerd. `obj=` of `sel=`.

Paden en namen van groepen/objecten zijn niet hoofdlettergevoelig.

## Standaard {#section-0c322850512c4896bb551856a549440e}

De eerste groep in het vignet die renderbare objecten bevat, wordt automatisch geselecteerd wanneer een nieuw vignet wordt geopend.

## Zie ook {#section-d9d2c92ef48548f48b9781e2a8a5fb5a}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b), [kenmerk::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
