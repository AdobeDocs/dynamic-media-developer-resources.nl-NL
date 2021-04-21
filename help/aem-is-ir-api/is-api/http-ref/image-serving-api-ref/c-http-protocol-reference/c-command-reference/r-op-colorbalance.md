---
description: De kleurbalans aanpassen. Hiermee wordt de waarde van elke RGB-kleurcomponent afzonderlijk aangepast.
solution: Experience Manager
title: op_kleurbalans
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---


# op_kleurbalans{#op-colorbalance}

De kleurbalans aanpassen. Hiermee wordt de waarde van elke RGB-kleurcomponent afzonderlijk aangepast.

`op_colorbalance= *``*, *``*, *`redAdjgreenAdjblueAdj`*`

<table id="simpletable_BBDAA6FE9A0E48E3BD8304BDED776713"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> redAdj</span> </p></td> 
  <td class="stentry"> <p>Afstelling van rode component (-100..+100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> greenAdj</span> </p></td> 
  <td class="stentry"> <p>Aanpassing van de groene component (-100..+100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> blueAdj</span> </p></td> 
  <td class="stentry"> <p>Aanpassing blauw onderdeel (-100..+100 int). </p></td> 
 </tr> 
</table>

Grijs- en CMYK-invoerafbeeldingsgegevens worden omgezet in RGB met behulp van native conversie. Dit is niet nauwkeurig wanneer kleurbeheer is ingeschakeld.

## Eigenschappen {#section-dff9c934f7c1442bbd02379b688d82e2}

Laag, opdracht. Wordt toegepast op de huidige laag of op de samengestelde afbeelding als `layer=comp`. Genegeerd door effectlagen. CMYK-afbeeldingen en -lagen worden omgezet in RGB voordat de bewerking wordt toegepast.

## Standaard {#section-08d84ef715964f7daea86f5ef237d199}

`op_colorbalance=0,0,0` voor geen kleurwijziging.

## Voorbeeld {#section-7e97fa36e01d4af8ab03fc9d493da1a1}

De kleurbalans naar rood duwen:

… `&op_colorBalance=100,0,0&`…
