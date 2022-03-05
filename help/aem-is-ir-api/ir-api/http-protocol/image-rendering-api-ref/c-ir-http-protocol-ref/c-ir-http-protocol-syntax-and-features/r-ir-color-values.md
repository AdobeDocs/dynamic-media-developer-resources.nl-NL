---
title: Kleurwaarden
description: Kleurwaarden voor de kenmerken color= en bgc= kunnen worden opgegeven met behulp van een lijst met decimale waarden, met komma's als scheidingsteken, of een hexadecimale notatie, vergelijkbaar met HTML.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 608ff0f1-4fbd-4e32-af07-3a62569d14c7
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 9%

---

# Kleurwaarden{#color-values}

Kleurwaarden voor `color=` en `bgc=` attributen kunnen worden gespecificeerd gebruikend of een lijst van decimale, komma-gescheiden componentenwaarden, of een hexadecimale aantekening, gelijkend op HTML.

<table id="simpletable_9B3A231D5BB14A3DB2B42B341E198341"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> kleur</span> </p></td> 
  <td class="stentry"> <p><span class="codeph">{ {red , green , blue} | grijs } | {[ 0x ] hex6 } | { 0xhex2}</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><i>rood, groen, blauw, grijs</i> </p></td> 
  <td class="stentry"> <p>Waarde van kleurcomponent (0...255, decimaal geheel getal). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><i>hex6</i> </p></td> 
  <td class="stentry"> <p>hexadecimale RGB-kleurwaarde (RRGGBB) van zes cijfers in pakket. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><i>hex2</i> </p></td> 
  <td class="stentry"> <p>Hexadecimale grijskleurwaarde (0...FF) in pakket van twee cijfers. </p></td> 
 </tr> 
</table>

## Voorbeelden {#section-a78732151d584e84abeb99f9ce8d7c24}

Enkele voorbeelden van geldige kleurspecificaties en de bijbehorende kleurwaardetoewijzing voor RGB:

<table id="simpletable_837B3173020240A5B7B2DB2F4CC57352"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 100 200 </p></td> 
  <td class="stentry"> <p>(0,100,200) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>128 </p></td> 
  <td class="stentry"> <p>(128 128 128) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0x010203 </p></td> 
  <td class="stentry"> <p>(1,2,3) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>00b1c2 </p></td> 
  <td class="stentry"> <p>(160 177 194) </p></td> 
 </tr> 
</table>

## Zie ook {#section-207d5cb918a94736a27445faa58917d3}

[color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa), [bgc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-bgc.md#reference-3f5c78cea01c4a85aa582076d23aebb0), [grot=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a)
