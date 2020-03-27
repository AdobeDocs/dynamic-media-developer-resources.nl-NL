---
description: Glansheid van het materiaaloppervlak. Hiermee bepaalt u de relatieve glans van het materiaaloppervlak. Hiermee selecteert u de belichtingsafbeelding en bestuurt u de rendering van glanseffecten en 3D-reflecties.
seo-description: Glansheid van het materiaaloppervlak. Hiermee bepaalt u de relatieve glans van het materiaaloppervlak. Hiermee selecteert u de belichtingsafbeelding en bestuurt u de rendering van glanseffecten en 3D-reflecties.
seo-title: glanzen
solution: Experience Manager
title: glanzen
topic: Scene7 Image Serving - Image Rendering API
uuid: 3774e08b-d24e-4cf2-8719-32a21bb9bcb6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# glanzen{#gloss}

Glansheid van het materiaaloppervlak. Hiermee bepaalt u de relatieve glans van het materiaaloppervlak. Hiermee selecteert u de belichtingsafbeelding en bestuurt u de rendering van glanseffecten en 3D-reflecties.

`gloss= *`val`*`

<table id="simpletable_82166CA080AD401180404462FB2407D7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>Glans (0...100 percenten) of -1 voor de standaard (verwijzing) glanswaarde. </p></td> 
 </tr> 
</table>

Hogere glanswaarden veroorzaken doorgaans sterkere, scherpere reflecties en als glanseffecten zijn ingeschakeld in het vignet, worden spiegelende hooglichten op het oppervlak van het materiaal versterkt, vooral door het contrast van de belichting te verhogen. Elk materiaaltype ( `type=`) definieert een minimum- en een maximumrendereffect. Voor sommige materiaalsoorten (bv. wandpapier) `gloss=` heeft dit nauwelijks invloed op de vormgeving van het rendereffect, terwijl voor andere materiaalsoorten (bv. steen of keramiek) het effect aanzienlijk sterker is.

Als `illum=-1` en als in het vignet meerdere belichtingstoewijzingen worden gedefinieerd, `gloss=` selecteert u de verlichtingstoewijzing die wordt gebruikt voor de huidige renderbewerking. De renderer kiest de verlichtingskaart waarvan glanswaarde het dichtst bij de gespecificeerde glanswaarde is.

`gloss=-1` Hiermee selecteert u de referentiewaarde voor glanzen van de geselecteerde verlichtingskaart, zoals gedefinieerd in de weergave-eigenschappen van het vignet. Dit zorgt ervoor dat de verlichtingskaart precies zoals geschreven, zonder verdere wijziging wordt gebruikt, zelfs als de glansgevolgen worden toegelaten. Ook `illum=-1` als dat het geval is, wordt de referentiewaarde voor glanzen van de eerste verlichtingskaart in de vignetweergave gebruikt.

## Eigenschappen {#section-92c20c7890fc4aad8d1725d1a1f82da6}

Materiaalkenmerk. Genegeerd als het vignet geen meerdere verlichtingstoewijzingen definieert of als dit `illum=` is opgegeven, als het vignet geen 3D-reflectiegegevens bevat of als het huidige object geen 3D-reflecties ondersteunt of als glanseffecten zijn uitgeschakeld in het vignet.

## Standaard {#section-3722fb5f85c24bc29bdf9c92ce04e678}

`attribute::Gloss` als het materiaal is gebaseerd op een catalogusitem, anders de referentiegloeiwaarde van de standaardverlichtingskaart of de verlichtingskaart die door `illum=`.

## Zie ook {#section-29f5b761481a4c52a499a2e16e63c70b}

[kenmerk::Glans](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb), [type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35), [rough=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180), [glossmap=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a), [illum=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-illum.md#reference-8efe483a30684022bfe711eb73efbee6)
