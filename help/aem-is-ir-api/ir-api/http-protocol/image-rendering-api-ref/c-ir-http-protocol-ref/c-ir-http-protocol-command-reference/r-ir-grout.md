---
title: glanzen
description: Kleur en dikte van tegelkleurruimte. Hiermee simuleert u de grond voor keramische en natuurlijke stenen tegels.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6647b459-11d2-47e4-9033-3a740f01a623
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# glanzen {#grout}

Kleur en dikte van tegelkleurruimte. Hiermee simuleert u de grond voor keramische en natuurlijke stenen tegels.

grot= *`color`*[,*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> kleur </span> </span> </p> </td>
  <td class="stentry"> <p>Groeperingskleur (grijs of RGB). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td>
  <td class="stentry"> <p>Gegroepeerde dikte; coördinaten van scènes (doorgaans inches) (reëel). </p> </td>
 </tr> 
</table>

Voor maximale controle van de vormgeving van de tussenruimte gelden de volgende voorschriften:

* De tegel moet vierkant of rechthoekig zijn; momenteel worden geen andere vormen ondersteund.
* De afbeelding mag slechts één tegel bevatten.
* De standaardruimte in de afbeelding (indien aanwezig) moet dezelfde dikte hebben op alle vier de randen.
* De dikte van de standaardtussenruimte moet in de materiaalcatalogus worden opgegeven ( `catalog::GroutWidth`).

## Eigenschappen {#section-de78b678245b4ffda48097c345949e77}

Materiaalkenmerk. `*`kleur`*` Dit moet een kleurwaarde voor RGB zijn. `*`width`*` moet een reële waarde 0 of hoger zijn.

Genegeerd als repeat = 4, 5, 7, 8, 9, 14 of hoger, of wanneer gespecificeerd voor andere materialen dan herhaalbare structuren.

## Standaard {#section-bfab3621f70b4489a21994ab11b20cc6}

Indien `grout=` niet is opgegeven, wordt de tussenruimte in de afbeelding niet gewijzigd. Indien `grout= *`kleur`*` is gespecificeerd, `*`width`*` standaardinstellingen `catalog::GroutWidth`.

## Zie ook {#section-8d472906a44943f5a8557e98f2fbc71f}

[Kleurwaarden](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
