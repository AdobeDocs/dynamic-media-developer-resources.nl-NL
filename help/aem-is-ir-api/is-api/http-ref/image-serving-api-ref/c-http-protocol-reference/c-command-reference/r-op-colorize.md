---
description: Afbeelding inkleuren. De afbeeldingsgegevens worden ingekleurd met behoud van schaduwen en hooglichten.
seo-description: Afbeelding inkleuren. De afbeeldingsgegevens worden ingekleurd met behoud van schaduwen en hooglichten.
seo-title: op_inkleuren
solution: Experience Manager
title: op_inkleuren
topic: Scene7 Image Serving - Image Rendering API
uuid: e74a85ca-73bf-4c69-ac77-768a58b33d0b
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# op_inkleuren{#op-colorize}

Afbeelding inkleuren. De afbeeldingsgegevens worden ingekleurd met behoud van schaduwen en hooglichten.

` op_colorize= *``*[,off|norm[, *`kleurcontrast`*]]`

<table id="simpletable_768D6CDF3F734E7F89DC7AB2EAAC0C77"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> kleur </span> </p> </td> 
  <td class="stentry"> <p>RGB-kleur vervangen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> uit </span> </p> </td> 
  <td class="stentry"> <p>Automatische helderheidscompensatie uitschakelen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> norm </span> </p> </td> 
  <td class="stentry"> <p>Automatische helderheidscompensatie inschakelen (standaardwaarde). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> contrast </span> </p> </td> 
  <td class="stentry"> <p>Contrastbereik (reëel 0..100); ingesteld op 0 om het invoercontrast te behouden. </p> </td> 
 </tr> 
</table>

Het tweede argument geeft aan of de helderheid van de bronafbeelding moet worden aangepast voordat deze wordt ingekleurd. Geef op `off` om de automatische helderheidscompensatie uit te schakelen of `norm` om de helderheid automatisch aan te passen, zodat de mediaanwaarde een intensiteit van 50% heeft.

Stel de *`contrast`* waarde in op 0 om het contrastbereik van de invoerafbeelding te behouden of geef een gewenst contrastbereik op met een waarde groter dan 0. Bij een waarde van 100 wordt het contrast gemaximaliseerd. De typische waarden kunnen tussen 30 en 70 zijn.

Naast de ingebouwde aanpassingen van de helderheid en het contrast, `op_brightness=` en kan `op_contrast=` worden gebruikt om het het inkleven effect verder te verfijnen.

>[!NOTE]
>
>Het inkleuringsalgoritme gebruikt alleen de luminantie-informatie in de afbeeldingsgegevens. Deze omzetting in grijswaarden is eenvoudig en er wordt geen kleurbeheer op toegepast. `op_colorize` voert RGB-gegevens altijd uit, zelfs als de invoer grijswaarden of CMYK is.

## Eigenschappen {#section-c0f8bd424b864153a1108f384939f55b}

Laag, opdracht. Is van toepassing op de huidige laag of op de samengestelde afbeelding, indien van toepassing `layer=comp`. Genegeerd door effectlagen.

*`color`* moet een RGB-waarde zijn; grijswaarden of CMYK- *`color`* waarden worden niet ondersteund.

De *`contrast`* waarde wordt genegeerd als helderheidscompensatie wordt uitgezet.

*`color`* wordt aangenomen dat deze voorkomt in de werkkleurruimte die overeenkomt met het pixeltype van *`color`*. *`color`* nauwkeurig wordt omgezet als de laagafbeelding een ander pixeltype heeft op het moment van samenvoegen.

CMYK-afbeeldingen worden omgezet in RGB voordat de bewerking wordt toegepast.

## Standaard {#section-0c3ea13efbac432c8970862d223e39b3}

`None`voor geen inkleuring. Het tweede en derde argument worden standaard ingesteld op `norm,0`, voor automatische helderheidscompensatie en geen contrastwijziging.

## Voorbeeld {#section-4c418d7b5e97409d9a448b8f08a1eab3}

Pas de helderheid en het contrast dynamisch aan voordat u een afbeeldingslaag inkleurt:

… `&op_brightness=-15&op_contrast=22&op_colorize=a0b0c0&`…

Gebruik in plaats hiervan automatische aanpassing van helderheid en contrast:

… `&op_colorize=a0b0c0,norm,50&`…

## Zie ook {#section-5581eb0e03014fa795e8f078c60e6c8d}

[color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [op_brightness=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-brightness.md#reference-edf79dc41ae5411c80bec3ee3731c58a), [op_contrast=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-contrast.md#reference-b26dfa9869fd43bebea0fbb8e9fe743d), [Kleurbeheer](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
