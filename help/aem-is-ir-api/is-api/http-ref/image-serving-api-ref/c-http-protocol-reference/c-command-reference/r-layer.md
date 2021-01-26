---
description: Selecteer Laag. Selecteert een laag en begint een nieuw segment van de laagdefinitie in de bevelopeenvolging.
seo-description: Selecteer Laag. Selecteert een laag en begint een nieuw segment van de laagdefinitie in de bevelopeenvolging.
seo-title: laag
solution: Experience Manager
title: laag
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 882309b3-51d7-477e-bd09-068ce9e55eb5
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 0%

---


# laag{#layer}

Selecteer Laag. Selecteert een laag en begint een nieuw segment van de laagdefinitie in de bevelopeenvolging.

`layer= *``*|comp[, *`naam`*]`

`layer= *`name`*`

<table id="simpletable_22DE3365A6454949B0D30C6D7110476E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p></td> 
  <td class="stentry"> <p>Aantal te selecteren laag (0 of groter int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> samenstellen</span> </p></td> 
  <td class="stentry"> <p>Selecteer de samengestelde afbeelding. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> name</span></span> </p></td> 
  <td class="stentry"> <p>Laagnaam. </p></td> 
 </tr> 
</table>

Alle opdrachten in het laagsegment worden toegepast op de opgegeven laag. Een laagsegment wordt geëindigd door volgende `layer=` of `effect=` bevel of het eind van het verzoek.

Geef `layer=comp` op om de samengestelde afbeelding (of weergave voor sommige opdrachten) te selecteren.

Met het laagnummer wordt de z-volgorde voor de laag opgegeven. De lagen met een hoger nummer worden boven op de lagen met een lager nummer geplaatst.

Laagnummers hoeven niet opeenvolgend te zijn. Laag 0 wordt vereist.

Een naam kan aan een laag met `layer= *`n`*, *`name`*` bevelvariant worden toegewezen. Zodra een genoemde laag wordt bepaald, kan het met ` layer= *`name`*` worden van verwijzingen voorzien, zonder het moeten het laagaantal kennen. De veelvoudige namen kunnen aan de zelfde laag worden toegewezen, gebruikend veelvoudige `layer= *`n`*, *`name`*` bevelen.

>[!NOTE]
>
>Laag 0 bepaalt de algemene grootte van het samengestelde canvas. Alle delen van lagen die buiten de grenzen van laag 0 vallen worden afgesneden wanneer de samenstelling wordt gebouwd.

## Eigenschappen {#section-499963ee52c14f2898f0d0f90c1d01be}

Laag, opdracht. Verwijzingen naar vervangingsvariabelen worden niet ondersteund in `layer=`.

`comp` is niet toegestaan als een  *`name`* tekenreeks. Er wordt een fout geretourneerd als dezelfde *`name`* aan meerdere lagen is toegewezen of als naar een laag wordt verwezen door *`name`* die niet eerder is gedefinieerd.

## Standaard {#section-091859a03f8048c2b7092f0fec9c1006}

`layer=comp`. Veel opdrachten en kenmerken zijn van toepassing op laag 0 als `layer=comp`.

## Speciale gevallen {#section-e087cb2e3562473e8d391abfa3b9489f}

* Als dezelfde naam aan meerdere lagen is toegewezen (bijvoorbeeld: `layer=1,image&layer=2,image`), treedt een fout op.
* Als dezelfde naam meerdere malen aan één laag is toegewezen (bijvoorbeeld: `layer=1,image&layer=1,image`), wordt werkingsgebied geplaatst zoals gewoonlijk, zonder fouten.
* Meerdere namen voor dezelfde laag worden ondersteund.

   U kunt een van de namen gebruiken om naar de laag te verwijzen (bijvoorbeeld: `layer=1,image&layer=1,picture`).
* Als een naam waarnaar wordt verwezen nooit wordt toegewezen aan een laagnummer (bijvoorbeeld: `layer=1,image&layer=picture`), treedt een fout op.
* Vervangende variabelen worden niet ondersteund in laagmodifiers (bijvoorbeeld: `layer=$image$`).

   Dit geldt voor alle permutaties, niet alleen voor laagnamen maar ook voor laagmodifiers in het algemeen.

* Alle regels voor samenvoegen en overschrijven werken precies zo als wanneer in meerdere bronnen naar dezelfde laag wordt verwezen (aanvraag, catalogusrecords vóór of na wijziging, macro&#39;s, enz.).

## Voorbeeld {#section-cc40de6a0a754178aa752601539c815b}

Zie de voorbeelden in [Sjablonen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).
