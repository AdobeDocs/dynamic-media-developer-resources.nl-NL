---
title: Scherp
description: Standaardmateriaalverscherping. Hiermee stelt u de standaardmateriaalverscherpingsmodus in voor het geval een bepaalde catalogusrecord geen geldige waarde voor Verscherpen catalogus bevat.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fe8f7662-bfa1-43bf-ab66-5de5598edcd4
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 4%

---

# Scherp{#sharp}

Standaardmateriaalverscherping. Hiermee wordt de standaardmateriaalverscherpingsmodus ingesteld voor het geval een bepaalde catalogusrecord geen geldige waarde bevat `catalog::Sharp` waarde.

## Eigenschappen {#section-dcb810d01b8a40eb991d555a3cbe48b9}

Enum.

<table id="simpletable_2D94A380BC2D4FD1A7EDD45E6EAFD1FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Geen verscherping. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Normale verscherping (na de transformatie). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Alternatieve verscherping (vóór de transformatie). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Meer verscherping (zowel voor als na de transformatie). </p> </td> 
 </tr> 
</table>

## Standaard {#section-613130fca7c04ce7a7734265f27aa1ea}

Overgenomen van `default::Sharp` indien niet gedefinieerd of leeg.

## Zie ook {#section-7771824f2822443ab0297e8793bb48ae}

[catalogus::Scherp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) , [shar=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a), [catalogus:RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
