---
title: landinstelling
description: Landinstellings-id voor vertaling. Geeft de landinstellings-id voor de aanvraag op.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d937dfa5-95dd-49fd-ac23-e77e07b0642c
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---

# landinstelling{#locale}

Landinstellings-id voor vertaling. Geeft de landinstellings-id voor de aanvraag op.

`locale=[ *`locId`*]`

<table id="simpletable_C1899AD02C984ED3896B7620916637E7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> locId</span></span> </p> </td> 
  <td class="stentry"> <p>Landinstelling-id (tekenreeks). </p></td> 
 </tr> 
</table>

Gebruikend deze identiteitskaart en de regels die met worden gespecificeerd `attribute::LocaleMap` en `attribute::LocaleStrMap`, Image Serving past optionele vertaling van catalogus-id en lokalisatie van tekenreeksen toe.

## Eigenschappen {#section-1854a9902b884d9b8e8e713b6635723f}

Verzoek, opdracht. Is op het volledige verzoek van toepassing, met inbegrip van genestelde/ingebedde verzoeken, ongeacht waar het wordt gespecificeerd. `locId` mag alleen afdrukbare ASCII-tekens bevatten. Genegeerd als er geen lokalisatiekaarten zijn gedefinieerd in de hoofdcatalogus van deze aanvraag. Er wordt een fout geretourneerd als deze leeg of ongeldig is `locId` is opgegeven en er is geen standaardregel gedefinieerd in `attribute::DefaultLocale`.

## Standaard {#section-9699fbc26de6453e9029e0003c79a7ef}

`attribute::DefaultLocale` wordt gebruikt wanneer locale= niet is opgegeven.

## Zie ook {#section-28a586d43ac4429d98e318a580c92af4}

[kenmerk::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b) , [kenmerk:LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [kenmerk:LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e), Localisatie-ondersteuning
