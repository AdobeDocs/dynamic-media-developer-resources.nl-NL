---
title: glanzen
description: Glansheid van het materiaaloppervlak. Hiermee bepaalt u de relatieve glans van het materiaaloppervlak. Hiermee selecteert u de belichtingsafbeelding en bestuurt u de rendering van glanseffecten en 3D-reflecties.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6df6cd05-9462-4c1e-a7ac-efac3461cf11
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 0%

---

# glanzen{#gloss}

Glansheid van het materiaaloppervlak. Hiermee bepaalt u de relatieve glans van het materiaaloppervlak. Hiermee selecteert u de belichtingsafbeelding en bestuurt u de rendering van glanseffecten en 3D-reflecties.

`gloss= *`val`*`

<table id="simpletable_82166CA080AD401180404462FB2407D7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>Glans (0...100 percenten) of -1 voor de standaard (verwijzing) glanswaarde. </p></td> 
 </tr> 
</table>

Hogere glanswaarden veroorzaken doorgaans sterkere, scherpere reflecties en als glanseffecten zijn ingeschakeld in het vignet, worden spiegelende hooglichten op het oppervlak van het materiaal versterkt, vooral door het contrast van de belichting te verhogen. Elk materiaaltype ( `type=`) definieert een minimum- en een maximum-rendereffect. Voor sommige materiaalsoorten (bijvoorbeeld wandpapier): `gloss=` heeft een minimale invloed op het uiterlijk van het rendereffect, terwijl het effect voor andere materiaalsoorten (bijvoorbeeld steen of keramiek) aanzienlijk duidelijker is.

Indien `illum=-1` en als het vignet meerdere verlichtingstoewijzingen definieert, `gloss=` Hiermee selecteert u de verlichtingskaart die wordt gebruikt voor de huidige renderbewerking. De renderer kiest de verlichtingskaart waarvan glanswaarde het dichtst bij de gespecificeerde glanswaarde is.

`gloss=-1` Hiermee selecteert u de referentiewaarde voor glanzen van de geselecteerde verlichtingskaart, zoals gedefinieerd in de weergave-eigenschappen van het vignet. Deze waarde zorgt ervoor dat de verlichtingskaart precies zoals geschreven, zonder verdere wijziging wordt gebruikt, zelfs als de glansgevolgen worden toegelaten. Indien `illum=-1` vervolgens wordt de referentiewaarde voor glanzen van de eerste verlichtingskaart in de vignetweergave gebruikt.

## Eigenschappen {#section-92c20c7890fc4aad8d1725d1a1f82da6}

Materiaalkenmerk. Genegeerd als in het vignet geen meerdere verlichtingstoewijzingen zijn gedefinieerd. Of, als `illum=` wordt opgegeven als het vignet geen 3D-reflectiegegevens bevat. Of als het huidige object geen 3D-reflecties ondersteunt of als glanseffecten zijn uitgeschakeld in het vignet.

## Standaard {#section-3722fb5f85c24bc29bdf9c92ce04e678}

`attribute::Gloss` Als het materiaal is gebaseerd op een catalogusitem, anders de referentiegalnewaarde van de standaardverlichtingskaart of de verlichtingskaart gespecificeerd door `illum=`.

## Zie ook {#section-29f5b761481a4c52a499a2e16e63c70b}

[kenmerk:Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb), [type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35), [hard=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180), [glossmap=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a), [illum=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-illum.md#reference-8efe483a30684022bfe711eb73efbee6)
