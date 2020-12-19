---
description: Weergavebreedte. Hiermee geeft u de breedte op van de reactieafbeelding (weergaveafbeelding) wanneer fit= niet aanwezig is in de aanvraag.
seo-description: Weergavebreedte. Hiermee geeft u de breedte op van de reactieafbeelding (weergaveafbeelding) wanneer fit= niet aanwezig is in de aanvraag.
seo-title: winderig
solution: Experience Manager
title: winderig
topic: Scene7 Image Serving - Image Rendering API
uuid: 30aeeea0-c8c9-40b9-a244-2802a7102dd6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 0%

---


# wid{#wid}

Weergavebreedte. Hiermee geeft u de breedte op van de reactieafbeelding (weergaveafbeelding) wanneer fit= niet aanwezig is in de aanvraag.

` wid= *`val`*`

<table id="simpletable_E217453246F5441C896C1F69EA4D4218"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>Afbeeldingsbreedte in pixels (int groter dan 0). </p> </td> 
 </tr> 
</table>

Als zowel `hei=` als `scl=` worden gespecificeerd, kan het samengestelde beeld volgens het `align=` attribuut worden bebouwd. Wanneer `fit=` aanwezig is, `wid=` specificeert de nauwkeurige, de minimum, of de maximumbreedte van het reactiebeeld; Raadpleeg de beschrijving van `fit=` voor meer informatie.

Als `scl=` niet is opgegeven, wordt de samengestelde afbeelding passend geschaald. Als zowel `wid=` als `hei=` worden gespecificeerd, en `scl=` niet wordt gespecificeerd, dan wordt het beeld geschraapt om volledig binnen de wid/hei rechthoek te passen, verlatend zo weinig mogelijk achtergrondoppervlak. In dit geval wordt de afbeelding binnen de weergaverechthoek geplaatst volgens het kenmerk `align=`.

>[!NOTE]
>
>Er wordt een fout geretourneerd als de berekende of standaardgrootte van de antwoordafbeelding groter is dan `attribute::MaxPix`.

## Standaard {#section-976d4c8554a34c899f85d172f6ac6f58}

Als noch `wid=`, `hei=`, noch `scl=` worden gespecificeerd, zal het antwoordbeeld of de grootte van het samengestelde beeld of `attribute::DefaultPix` hebben, welke kleiner is.

## Eigenschappen {#section-c93b7ce1b0d2475f80b06264b45d1285}

Kenmerk weergeven. Is van toepassing ongeacht de huidige laaginstelling.

## Voorbeeld {#section-82bc98b7c15a451bbe9b915d414c0470}

een afbeelding aanvragen om in een rechthoek van 200 x 200 te passen; de afbeelding wordt rechtsboven uitgelijnd als deze niet vierkant is. Een willekeurig achtergrondgebied wordt gevuld met `attribute::BkgColor`.

` http:// *`server`*/myRootId/myImageId?wid=200&hei=200&align=1,-1`

Dezelfde afbeelding, geleverd met een vaste breedte van 200 pixels, maar met een variabele hoogte om de hoogte-breedteverhouding van de afbeelding te behouden. In dit geval heeft de geretourneerde afbeelding nooit een opvulgebied voor de achtergrond. Let erop dat align= in dit geval helemaal geen effect heeft.

` http:// *`server`*/myRootId/myImageId?wid=200`

## Zie ook {#section-4e9659238d6545498378ca8b1f3ec4ae}

[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96) ,  [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7),  [kenmerk::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1),  [kenmerk::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
