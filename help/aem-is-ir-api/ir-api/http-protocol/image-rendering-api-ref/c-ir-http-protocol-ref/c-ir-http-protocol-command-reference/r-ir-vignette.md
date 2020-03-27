---
description: Vignetbestand. Geeft het vignet op dat voor deze aanvraag moet worden gebruikt.
seo-description: Vignetbestand. Geeft het vignet op dat voor deze aanvraag moet worden gebruikt.
seo-title: vignet
solution: Experience Manager
title: vignet
topic: Scene7 Image Serving - Image Rendering API
uuid: 8bba4ad4-bd55-4c55-8ebf-585371cf33f1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# vignet{#vignette}

Vignetbestand. Geeft het vignet op dat voor deze aanvraag moet worden gebruikt.

`vignette=[ *``*/] *``*|[catId/] *`catIdrecIdfile`*`

<table id="simpletable_432EC5501CA3431B83A762C3EE4E8DD2"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p> </td> 
  <td class="stentry"> <p>Materiaalcatalogus-id (komt overeen met <span class="codeph"> kenmerk::RootId</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>Vignet-id (komt overeen met <span class="codeph"> vignet::Id</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> file</span> </p></td> 
  <td class="stentry"> <p>Relatief pad en naam voor vignetbestand. </p></td> 
 </tr> 
</table>

U kunt een item voor een vignetkaart of een vignetbestand opgeven. Externe URL&#39;s zijn niet toegestaan.

`vignette=` kan worden gebruikt als alternatief voor het opgeven van het vignet in het verzoek-URL-pad. Wordt voornamelijk gebruikt om vignetten via variabelen in sjablonen op te geven.

Als *`catId`* niet is opgegeven, wordt de sessiecatalogus gebruikt.

## Eigenschappen {#section-f58661fc78d7496e8e3d0fb98b945c4b}

Kan overal binnen het verzoek voorkomen. Hiermee overschrijft u het vignet dat is opgegeven met het verzoek-URL-pad.

## Standaard {#section-db0618d48bc84dc8abcc989550349ccc}

Geen.

## Zie ook {#section-dc2668cc2cd54a74b08cff68a12d4edd}

[Materiaalcatalogi](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2), [aangepaste variabelen](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-custom-variables/c-ir-custom-variables.md#concept-8a1d9a50d09a4b7b97b8c83365971f96)
