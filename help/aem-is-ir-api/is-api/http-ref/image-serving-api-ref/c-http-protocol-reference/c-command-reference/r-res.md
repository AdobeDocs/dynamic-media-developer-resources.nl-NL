---
description: Afbeeldingen schalen op basis van resolutie. Hiermee schaalt u de afbeelding naar de gewenste resolutie.
seo-description: Afbeeldingen schalen op basis van resolutie. Hiermee schaalt u de afbeelding naar de gewenste resolutie.
seo-title: res
solution: Experience Manager
title: res
topic: Scene7 Image Serving - Image Rendering API
uuid: ab0c8329-5d40-4233-a122-8cb8ca01b500
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---


# res{#res}

Afbeeldingen schalen op basis van resolutie. Hiermee schaalt u de afbeelding naar de gewenste resolutie.

` res= *`val`*`

<table id="simpletable_E69F3709266749C4A165C90FF18FF5AA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>doelresolutie; meestal in pixels per inch (reëel). </p> </td> 
 </tr> 
</table>

De schaalfactor wordt berekend door *`val`* te delen door `catalog::Resolution`. Deze opdracht heeft geen invloed op de afdrukresolutie van de antwoordafbeelding.

Als u deze functie wilt gebruiken, moet de resolutie van de oorspronkelijke bronafbeeldingen bekend zijn en worden ingesteld in `catalog::Resolution`. Afhankelijk van de toepassing kunnen de resolutie-eenheden variëren. Voor herhaalbare 2D-structuren of materiaalstalen, zoals achtergronden of weefsels, kan de resolutie worden uitgedrukt in pixels/inch of pixels/mm. Luchtfoto&#39;s en kaarten kunnen beter worden bediend door pixels/mijl of pixels/km. In elk geval moeten de eenheden die voor `catalog::Resolution` worden gebruikt, dezelfde zijn als de eenheden die voor `res=` worden gebruikt.

Naast het verkrijgen van afbeeldingen met nauwkeurige resoluties, kan `res=` ook worden gebruikt om meerdere afbeeldingen met dezelfde resolutie te combineren, zodat de items die zichtbaar zijn in deze afbeeldingen in nauwkeurige verhouding tot elkaar staan.

>[!NOTE]
>
>Normaal gesproken wordt de grootte van een samengestelde afbeelding aangepast aan de grootte van de doelweergave (opgegeven door `wid=`, `hei=` of `attribute::DefaultPix`) voordat deze wordt geretourneerd naar de client. Als u dit wijzigen van de grootte wilt voorkomen en een afbeelding wilt verkrijgen met de exacte resolutie die wordt opgegeven door `res=`, kan het nodig zijn om de schaling van de weergave uit te schakelen door `scl=1` expliciet op te geven. Hierdoor wordt de server opgedragen de samengestelde afbeelding bij te snijden naar de grootte van de doelweergave in plaats van deze te schalen.

## Eigenschappen {#section-fdbd16e59cff4952a3717146bc91412e}

Kenmerk van bronafbeelding/masker. Genegeerd door lagen die niet aan een bronafbeelding of -masker zijn gekoppeld. Toegepast op laag 0 wordt gespecificeerd voor `layer=comp`. Wordt genegeerd als `scale=` of `size=` voor dezelfde laag is opgegeven.

## Standaard {#section-c5f1ba6fe53d46eca32e7d0588dcdf3d}

Indien niet opgegeven, bepaalt `scale=` of `size=` de schaalfactor, of als geen van beide is opgegeven, wordt de afbeelding zonder schaling gebruikt.

## Voorbeeld {#section-eb06f333e08e4247971fb1b18922597b}

Haal een structuurafbeelding op van 12 pixels/inch voor gebruik met Afbeelding renderen of Afbeelding ontwerpen. We geven een PNG-indeling zonder verlies en een betere kwaliteit bij het berekenen van het aantal pixels voor een optimale kwaliteit,

` http:// *`server`*/myTexture?res=12&fmt=png&resMode=sharp`

## Zie ook {#section-1f8a8f11772e493ca803c4511f397a11}

[catalog::Resolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1) ,  [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
