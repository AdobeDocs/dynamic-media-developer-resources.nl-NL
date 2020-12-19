---
description: Kleur en dikte van tegelkleurruimte. Hiermee simuleert u de grond voor keramische en natuurlijke stenen tegels.
seo-description: Kleur en dikte van tegelkleurruimte. Hiermee simuleert u de grond voor keramische en natuurlijke stenen tegels.
seo-title: glanzen
solution: Experience Manager
title: glanzen
topic: Scene7 Image Serving - Image Rendering API
uuid: 00069004-40f2-4ab6-85d8-ca197b7bef69
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---


# tussenruimte{#grout}

Kleur en dikte van tegelkleurruimte. Hiermee simuleert u de grond voor keramische en natuurlijke stenen tegels.

grout= *`color`*[,*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> kleur  </span> </span> </p> </td> 
  <td class="stentry"> <p>Kleur van groep (grijs of RGB). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width  </span> </span> </p> </td> 
  <td class="stentry"> <p>Gegroepeerde dikte; coördinaten van scènes (doorgaans inches) (reëel). </p> </td> 
 </tr> 
</table>

Voor een maximale controle van de vormgeving van de grond gelden de volgende voorschriften:

* De tegel moet vierkant of rechthoekig zijn; momenteel worden geen andere vormen ondersteund.
* De afbeelding mag slechts één tegel bevatten.
* De standaardruimte in de afbeelding (indien aanwezig) moet exact dezelfde dikte hebben op alle vier de randen.
* De dikte van de standaardtussenruimte moet worden opgegeven in de materiaalcatalogus ( `catalog::GroutWidth`).

## Eigenschappen {#section-de78b678245b4ffda48097c345949e77}

Materiaalkenmerk. ` *`moet een RGB-kleurwaarde `*` zijn. ` *`De `*` breedte moet een reële waarde 0 of groter zijn.

Genegeerd als repeat = 4, 5, 7, 8, 9, 14 of hoger, of wanneer gespecificeerd voor andere materialen dan herhaalbare structuren.

## Standaard {#section-bfab3621f70b4489a21994ab11b20cc6}

Als `grout=` niet wordt gespecificeerd, wordt de grond in het beeld niet gewijzigd. Als ` grout= *`color`*` is opgegeven, wordt ` *`width`*` standaard ingesteld op `catalog::GroutWidth`.

## Zie ook {#section-8d472906a44943f5a8557e98f2fbc71f}

[Kleurwaarden](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
