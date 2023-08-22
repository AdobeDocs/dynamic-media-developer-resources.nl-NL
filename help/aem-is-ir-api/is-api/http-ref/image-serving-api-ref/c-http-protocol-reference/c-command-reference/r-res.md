---
title: res
description: Op resolutie gebaseerde afbeeldingsschaling. Hiermee schaalt u de afbeelding naar de gewenste resolutie.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e8ed7b00-7bb3-463e-9aaa-47f77bd4b45e
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 0%

---

# res{#res}

Op resolutie gebaseerde afbeeldingsschaling. Hiermee schaalt u de afbeelding naar de gewenste resolutie.

` res= *`val`*`

<table id="simpletable_E69F3709266749C4A165C90FF18FF5AA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>Doelresolutie; doorgaans in pixels per inch (reëel). </p> </td> 
 </tr> 
</table>

De schaalfactor wordt berekend door deze te delen *`val`* door `catalog::Resolution`. Deze opdracht heeft geen invloed op de afdrukresolutie van de antwoordafbeelding.

Als u deze functie wilt gebruiken, moet de resolutie van de oorspronkelijke bronafbeeldingen bekend zijn en zijn ingesteld in `catalog::Resolution`. Afhankelijk van de toepassing kunnen de resolutie-eenheden variëren. Voor herhaalbare 2D-structuren of materiaalstalen, zoals achtergronden of weefsels, kan de resolutie worden uitgedrukt in pixels/inch of pixels/mm. Luchtfoto&#39;s en kaarten kunnen beter worden bediend door pixels/mijl of pixels/km. In ieder geval de eenheden die worden gebruikt voor `catalog::Resolution` moet dezelfde zijn als de eenheden die worden gebruikt voor `res=`.

Naast het verkrijgen van beelden met nauwkeurige resoluties, `res=` kunt u ook gebruiken om meerdere afbeeldingen met dezelfde resolutie te combineren, zodat de items die in deze afbeeldingen zichtbaar zijn, in de juiste verhouding tot elkaar staan.

>[!NOTE]
>
>Normaal gesproken wordt de grootte van een samengestelde afbeelding aangepast aan de grootte van de doelweergave (opgegeven door `wid=`, `hei=`, of `attribute::DefaultPix`) voordat deze aan de client wordt geretourneerd. Als u dit niet wilt vergroten of verkleinen en een afbeelding wilt verkrijgen met de exacte resolutie die wordt opgegeven door `res=`, kan het nodig zijn om weergaveschaling uit te schakelen door expliciet `scl=1`. Hierdoor wordt de server opgedragen de samengestelde afbeelding bij te snijden naar de grootte van de doelweergave in plaats van deze te schalen.

## Eigenschappen {#section-fdbd16e59cff4952a3717146bc91412e}

Kenmerk van bronafbeelding/masker. Genegeerd door lagen die niet aan een bronafbeelding of -masker zijn gekoppeld. Toegepast op laag 0 is opgegeven voor `layer=comp`. Genegeerd als een van beide `scale=` of `size=` wordt opgegeven voor dezelfde laag.

## Standaard {#section-c5f1ba6fe53d46eca32e7d0588dcdf3d}

Indien niet opgegeven, `scale=` of `size=` Hiermee bepaalt u de schaalfactor. Als geen van beide is opgegeven, wordt de afbeelding zonder schaling gebruikt.

## Voorbeeld {#section-eb06f333e08e4247971fb1b18922597b}

Haal een structuurafbeelding op van 12 pixels/inch voor gebruik met Afbeelding renderen of Afbeelding ontwerpen. We geven een PNG-indeling zonder verlies en een betere kwaliteit bij het berekenen van het aantal pixels voor een optimale kwaliteit,

` http:// *`server`*/myTexture?res=12&fmt=png&resMode=sharp`

## Zie ook {#section-1f8a8f11772e493ca803c4511f397a11}

[catalogus:Resolutie](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1) , [kenmerk::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
