---
description: Hoogte weergeven. Hiermee geeft u de hoogte op van de reactieafbeelding (weergaveafbeelding) wanneer fit niet aanwezig is in de aanvraag.
seo-description: Hoogte weergeven. Hiermee geeft u de hoogte op van de reactieafbeelding (weergaveafbeelding) wanneer fit niet aanwezig is in de aanvraag.
seo-title: hei
solution: Experience Manager
title: hei
topic: Scene7 Image Serving - Image Rendering API
uuid: 307952bb-604f-49b4-bce3-b7a7fc7ec63b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 0%

---


# hei{#hei}

Hoogte weergeven. Hiermee geeft u de hoogte op van de reactieafbeelding (weergaveafbeelding) wanneer fit niet aanwezig is in de aanvraag.

` hei= *`val`*`

<table id="simpletable_1A36827B6E6647888A4E6E868975D716"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var  </span> </span> </p> </td> 
  <td class="stentry"> <p>Hoogte van afbeelding in pixels (int groter dan 0). </p> </td> 
 </tr> 
</table>

Als zowel `wid=` als `scl=` worden gespecificeerd, kan het samengestelde beeld volgens het `align=`attribuut worden bebouwd. Wanneer `fit=` aanwezig is, `hei=` specificeert de nauwkeurige, de minimum, of de maximumhoogte van het reactiebeeld; Raadpleeg de beschrijving van ` [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)` voor meer informatie.

Als `scl=` niet is opgegeven, wordt de samengestelde afbeelding passend geschaald. Als zowel `wid=` als `hei=` worden gespecificeerd, en `scl=` niet wordt gespecificeerd, dan wordt het beeld geschraapt om volledig binnen de wid/hei rechthoek te passen, verlatend zo weinig mogelijk achtergrondgebied blootstellend; in dit geval wordt de afbeelding binnen de weergaverechthoek geplaatst volgens het `align=`-kenmerk. Het achtergrondgebied wordt gevuld met `bgc=` of, indien niet opgegeven met `attribute::BkgColor`.

>[!NOTE]
>
>Er wordt een fout geretourneerd als de berekende grootte van de antwoordafbeelding groter is dan `attribute::MaxPix`.

## Eigenschappen {#section-534923644a1e464496eeba83dedcbd3c}

Kenmerk weergeven. Is van toepassing ongeacht de huidige laaginstelling.

## Standaard {#section-76544d34806d4124a8b173e229cba71f}

Als noch `wid=`, `hei=`, noch `scl=` worden gespecificeerd, heeft het antwoordbeeld of de grootte van het samengestelde beeld of `attribute::DefaultPix`, welke kleiner is.

## Voorbeelden {#section-eb10df7cd67e4733984810aaffd0b9e2}

een afbeelding aanvragen om in een rechthoek van 200 x 200 te passen; de afbeelding wordt links boven uitgelijnd als deze niet vierkant is. Een willekeurig achtergrondgebied wordt gevuld met `attribute::BkgColor`.

`http://server/myRootId/myImageId?wid=200&hei=200&align=-1,-1`

Dezelfde afbeelding, geleverd op een vaste hoogte van 200 pixels, maar met een variabele breedte die overeenkomt met de hoogte-breedteverhouding van de afbeelding. In dit geval heeft de geretourneerde afbeelding nooit een opvulgebied voor de achtergrond. In dit geval zou `align=` helemaal geen effect hebben.

`http://server/myRootId/myImageId?hei=200`

## Zie ook {#section-796e059e42ea4e86ab90ea3d024850ec}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7),  [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88),  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f)  [ ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)  [rgn=,attribute::DefaultPix,Attribut::MaxPixPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
