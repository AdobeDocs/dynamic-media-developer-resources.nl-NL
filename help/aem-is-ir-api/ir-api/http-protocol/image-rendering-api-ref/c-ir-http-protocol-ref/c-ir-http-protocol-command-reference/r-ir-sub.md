---
description: Subselectie. Hiermee kunt u verschillende materialen toepassen op verschillende gebieden van het geselecteerde object of de geselecteerde groep en eerder toegepaste materialen verwijderen.
solution: Experience Manager
title: sub
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 3%

---


# sub{#sub}

Subselectie. Hiermee kunt u verschillende materialen toepassen op verschillende gebieden van het geselecteerde object of de geselecteerde groep en eerder toegepaste materialen verwijderen.

`sub=0|1|2|3|4|5`

<table id="simpletable_F6BF91BD2C4B47BF8A28032E392D37F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Selecteer de hele muur. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Selecteer de bovenste helft van de muur. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>Selecteer de onderste helft van de muur. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Selecteer het bovenste randgebied van de muur. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>Selecteer het middelste gebied van de wandrand. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p> </td> 
  <td class="stentry"> <p>Selecteer het gebied van de onderrand van de muur. </p> </td> 
 </tr> 
</table>

Wordt momenteel alleen ondersteund voor wandobjecten. Beëindigt een voorafgaand MSS en begint een nieuw MSS voor het materiaal dat op de gespecificeerde sub-selectie moet worden toegepast.

Een materiaal dat voor of de hogere of lagere muur wordt gespecificeerd zal op de volledige muur van toepassing zijn tenzij een verschillend materiaal voor de andere helft van de muur ook is gespecificeerd.

## Eigenschappen {#section-b202139d6d0847cc8d520a154104ab9d}

Selectieopdracht; MSS-scheidingsteken.

## Standaard {#section-5b45a167a17c451596e4c59b7d53c368}

`sub=0`

## Zie ook {#section-1a993ee24f144d4fb8baef0cc431b53b}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)
