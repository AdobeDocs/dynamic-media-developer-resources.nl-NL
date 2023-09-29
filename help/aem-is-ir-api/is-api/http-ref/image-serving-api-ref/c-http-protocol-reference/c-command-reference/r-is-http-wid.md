---
title: winderig
description: Weergavebreedte. Hiermee geeft u de breedte op van de reactieafbeelding (weergaveafbeelding) wanneer fit= niet aanwezig is in de aanvraag.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ba22c79b-da59-4993-aa1c-2c990a0c4be5
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# winderig{#wid}

Weergavebreedte. Hiermee geeft u de breedte op van de reactieafbeelding (weergaveafbeelding) wanneer fit= niet aanwezig is in de aanvraag.

`wid= *`val`*`

<table id="simpletable_E217453246F5441C896C1F69EA4D4218"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>Afbeeldingsbreedte in pixels (int groter dan 0). </p> </td> 
 </tr> 
</table>

Als beide `hei=` en `scl=` worden opgegeven, kan de samengestelde afbeelding worden bijgesneden op basis van de `align=` kenmerk. Wanneer `fit=` aanwezig is, `wid=` geeft de exacte, minimale of maximale breedte van de reactieafbeelding aan; raadpleeg de beschrijving van `fit=` voor meer informatie.

Indien `scl=` niet is opgegeven, wordt de samengestelde afbeelding op maat geschaald. Als beide `wid=` en `hei=` gespecificeerd zijn, en `scl=` niet is opgegeven, wordt de afbeelding geschaald zodat deze volledig binnen de witte rechthoek past, zodat zo weinig mogelijk achtergrondoppervlak zichtbaar blijft. In dit geval wordt de afbeelding op basis van de `align=` kenmerk.

>[!NOTE]
>
>Er wordt een fout geretourneerd als de berekende of standaardgrootte van de antwoordafbeelding groter is dan `attribute::MaxPix`.

## Standaard {#section-976d4c8554a34c899f85d172f6ac6f58}

Als geen van beide `wid=`, `hei=`, noch `scl=` zijn opgegeven, heeft de antwoordafbeelding de grootte van de samengestelde afbeelding of `attribute::DefaultPix`, afhankelijk van welke waarde kleiner is.

## Eigenschappen {#section-c93b7ce1b0d2475f80b06264b45d1285}

Kenmerk weergeven. Deze wordt toegepast ongeacht de huidige laaginstelling.

## Voorbeeld {#section-82bc98b7c15a451bbe9b915d414c0470}

Vraag een afbeelding aan zodat deze past in een rechthoek van 200 x 200; lijn de afbeelding rechtsboven uit als deze niet vierkant is. Een willekeurig achtergrondgebied is gevuld met `attribute::BkgColor`.

` http:// *`Server`*/myRootId/myImageId?wid=200&hei=200&align=1,-1`

Dezelfde afbeelding, geleverd met een vaste breedte van 200 pixels, maar met een variabele hoogte om de hoogte-breedteverhouding van de afbeelding te behouden. In dit geval heeft de geretourneerde afbeelding nooit een opvulgebied voor de achtergrond. In dit geval: `align=` zou helemaal geen effect hebben.

` http:// *`Server`*/myRootId/myImageId?wid=200`

## Zie ook {#section-4e9659238d6545498378ca8b1f3ec4ae}

[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96) , [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [kenmerk::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [kenmerk::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
