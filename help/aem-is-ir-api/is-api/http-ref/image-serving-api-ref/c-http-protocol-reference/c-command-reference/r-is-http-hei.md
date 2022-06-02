---
description: Hoogte weergeven. Hiermee geeft u de hoogte op van de reactieafbeelding (weergaveafbeelding) wanneer fit niet aanwezig is in de aanvraag.
solution: Experience Manager
title: hei
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c812c7f0-4ac1-42cb-be47-7baebd8caf60
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# hei{#hei}

Hoogte weergeven. Hiermee geeft u de hoogte op van de reactieafbeelding (weergaveafbeelding) wanneer fit niet aanwezig is in de aanvraag.

` hei= *`val`*`

<table id="simpletable_1A36827B6E6647888A4E6E868975D716"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>Hoogte van afbeelding in pixels (int groter dan 0). </p> </td> 
 </tr> 
</table>

Als beide `wid=` en `scl=` worden opgegeven, kan de samengestelde afbeelding worden bijgesneden op basis van de `align=`kenmerk. Wanneer `fit=` aanwezig is, `hei=` geeft de exacte, minimale of maximale hoogte van het reactiebeeld aan; zie de beschrijving van [fit=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md) voor meer informatie.

Indien `scl=` niet is opgegeven, wordt de samengestelde afbeelding op maat geschaald. Als beide `wid=` en `hei=` gespecificeerd zijn, en `scl=` niet is opgegeven, wordt de afbeelding zodanig geschaald dat deze volledig binnen de rechthoek met schuine streep past, zodat zo weinig mogelijk achtergrondoppervlak zichtbaar blijft; in dit geval wordt de afbeelding binnen de weergaverechthoek geplaatst op basis van de `align=` kenmerk. Het achtergrondgebied is gevuld met `bgc=`of, indien niet gespecificeerd met `attribute::BkgColor`.

>[!NOTE]
>
>Er wordt een fout geretourneerd als de berekende grootte van de antwoordafbeelding groter is dan `attribute::MaxPix`.

## Eigenschappen {#section-534923644a1e464496eeba83dedcbd3c}

Kenmerk weergeven. Is van toepassing ongeacht de huidige laaginstelling.

## Standaard {#section-76544d34806d4124a8b173e229cba71f}

Als beide `wid=`, `hei=`, noch `scl=` opgegeven, heeft de antwoordafbeelding de grootte van de samengestelde afbeelding of `attribute::DefaultPix`, afhankelijk van welke waarde het kleinst is.

## Voorbeelden {#section-eb10df7cd67e4733984810aaffd0b9e2}

een afbeelding aanvragen om in een rechthoek van 200 x 200 te passen; de afbeelding wordt links boven uitgelijnd als deze niet vierkant is. Een willekeurig achtergrondgebied is gevuld met `attribute::BkgColor`.

`http://server/myRootId/myImageId?wid=200&hei=200&align=-1,-1`

Dezelfde afbeelding, geleverd op een vaste hoogte van 200 pixels, maar met een variabele breedte die overeenkomt met de hoogte-breedteverhouding van de afbeelding. In dit geval heeft de geretourneerde afbeelding nooit een opvulgebied voor de achtergrond. Let in dit geval op: `align=` zou helemaal geen effect hebben.

`http://server/myRootId/myImageId?hei=200`

## Zie ook {#section-796e059e42ea4e86ab90ea3d024850ec}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f), [kenmerk::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [kenmerk::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
