---
description: Rendering van afbeeldingen ondersteunt kleurruimteconversies op basis van kleurruimteprofielen die voldoen aan de ICC-specificatie (International Color Consortium).
seo-description: Rendering van afbeeldingen ondersteunt kleurruimteconversies op basis van kleurruimteprofielen die voldoen aan de ICC-specificatie (International Color Consortium).
seo-title: Kleurbeheer voor rendering van afbeeldingen *
solution: Experience Manager
title: Kleurbeheer voor rendering van afbeeldingen *
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9c47f584-645f-4eb7-bdc0-fdef459da3b2
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '761'
ht-degree: 0%

---


# Kleurbeheer bij renderen van afbeeldingen *{#image-rendering-color-management}

Rendering van afbeeldingen ondersteunt kleurruimteconversies op basis van kleurruimteprofielen die voldoen aan de ICC-specificatie (International Color Consortium).

**Beperkingen**

Momenteel worden alleen CMYK-, RGB- en grijswaardenkleurruimten ondersteund.

De dossiers van de kabinetstijl (.vnc) en de stijldossiers van vensterbekleding ( [!DNL .vnw]) zijn niet kleur-beheerd en verondersteld om in de het werk kleurenruimte te bestaan.

**Zie ook**

[International Color Consortium](http://www.color.org/index.xalter) ,  [ `icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06) ,  [ `iccEmbed=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f) ,  `attribute::IccProfile*` ,  `attribute::IccProfileSrc*`,  `attribute::IccRenderIntent` ,  `attribute::IccBlackPointCompensation` ,  `attribute::IccDither` ICC Profile Maps

## Standaardkleurruimten {#section-8ce27edf42e746febe4654f8f19b9c0c}

Elke afbeeldingscatalogus (en de standaardcatalogus) kunnen een set ICC-profielen definiëren. Deze profielen vormen de standaardkleurruimten voor deze catalogus: één invoer- en één uitvoerprofiel voor elk grijswaarden-, RGB- en CMYK-gegevens ( `attribute::IccProfileRgb`, `attribute::IccProfileGray`, `attribute::IccProfileCmyk`, `attribute::IccProfileSrcRgb`, `attribute::IccProfileSrcGray` en `attribute::IccProfileSrcCmyk`).

De standaardkleurruimte voor een bepaalde afbeelding of een ander object wordt geselecteerd in de standaardprofielen van de catalogus op basis van het pixeltype van de afbeelding.

## Invoerkleurruimte {#section-660f661a7e954df4b451e34134195276}

Materiële afbeeldingen kunnen ICC-profielen insluiten om de invoerkleurruimte te definiëren. Als er geen profiel is ingesloten in een bronafbeelding, wordt `attribute::IccProfileSrc*` van de toepasselijke afbeeldingscatalogus gebruikt die overeenkomt met het pixeltype van de bronafbeelding. Als dit kenmerk niet in de afbeeldingscatalogus is gedefinieerd, wordt `attribute::IccProfile*` gebruikt. Als dat cataloguskenmerk ook niet is gedefinieerd, wordt de afbeelding niet in kleur beheerd en worden alleen naïeve transformaties toegepast.

## Werkkleurruimte {#section-645d9cfa5b0347a190a0ece218f5b5e1}

De werkkleurruimte wordt meestal gedefinieerd door het ICC-kleurprofiel dat is ingesloten in het vignet. Als het vignet geen profiel bevat, wordt het standaard RGB-invoerprofiel ( `attribute::IccProfileSrcRgb` van de sessiecatalogus) gebruikt voor de werkkleurruimte.

Alle renderbewerkingen worden uitgevoerd in de werkkleurruimte.

**Belangrijk:** het ICC-profiel voor de werkkleurruimte moet invoer- en uitvoertransformaties ondersteunen. Als een alleen-uitvoerprofiel wordt gebruikt als werkkleurruimte, kan AIR materialen niet omzetten in een profiel. Een dergelijk kleurprofiel kan nog steeds worden gebruikt als de materialen zich in dezelfde werkkleurruimte bevinden. Het toepassen van materialen in andere kleurruimten mislukt.

## Expliciete kleurwaarden {#section-31727bf1b23e477ca92572fbbf422d2f}

RGB-kleurwaarden die worden opgegeven met `color=`, `bgc=`, `catalog::BgColor` en `catalog::Color`, worden verondersteld te bestaan in de huidige werkkleurruimte.

## Materiaalgegevensbestanden {#section-33f7a170a6664c02b8479fb89cc0aea3}

Materiaalafbeeldingsbestanden (structuur- en decale afbeeldingen) kunnen het pixeltype RGB, grijswaarden of CMYK hebben en kunnen een kleurprofiel insluiten. Als er geen kleurprofiel is ingesloten, wordt de standaardinvoerkleurruimte aan de afbeelding gekoppeld (bijvoorbeeld het kleurprofiel uit de materiaalcatalogus dat overeenkomt met het pixeltype van de afbeelding).

Materiaalafbeeldingen die worden verkregen bij verzoeken om geneste afbeeldingsserver of om het renderen van afbeeldingen, bevatten doorgaans een kleurprofiel. Als dit niet het geval is, worden de afbeeldingen gekoppeld aan de standaardinvoerkleurruimte die overeenkomt met het pixeltype.

Als de kleurruimte van het afbeeldingsbestand anders is dan de werkkleurruimte, wordt een nauwkeurige kleuromzetting gebruikt om de afbeelding om te zetten in de werkkleurruimte. Typeconversie zonder naam wordt gebruikt wanneer geen profiel is ingesloten en geen standaardinvoerprofiel is gedefinieerd.

Andere materiaalgegevensbestanden, zoals bestanden met CAB-stijl ( [!DNL .vnc]) of bestanden met vensterovervulling ( [!DNL .vnw]) sluiten geen kleurprofielen in en worden altijd verondersteld zich in de werkkleurruimte te bevinden.

## Uitvoerkleurruimte {#section-4c2c4dfedbb8429ba5cfddc3d3eab6c4}

Alle renderbewerkingen vinden plaats in de werkkleurruimte. Als in de aanvraag een ander kleurprofiel wordt opgegeven met de opdracht `icc=`, worden de gegevens naar die kleurruimte omgezet vlak voordat ze worden gecodeerd en naar de client worden geretourneerd. Als kleurbeheer is uitgeschakeld, wordt indien nodig naïeve omzetting gebruikt om de afbeelding om te zetten in grijswaarden of CMYK.

## Ingesloten kleurprofielen {#section-5ff733832d38429fbe02b3c1e9bb94a9}

Het kleurprofiel dat aan de gerenderde afbeelding is gekoppeld, kan in de reactieafbeelding worden ingesloten door `iccEmbed=` op te geven voor de aanvraag.

Als `icc=` niet is opgegeven, wordt het ICC-profiel voor de werkkleurruimte ingesloten. Er wordt geen profiel ingesloten als kleurbeheer is uitgeschakeld en er geen profiel is opgegeven met `icc=`.

## ICC-profielen {#section-afeb76068b5042adb83261638e450140}

Alle kleurprofielen die door de server worden gebruikt, moeten voldoen aan de ICC-specificatie. ICC-profielbestanden hebben doorgaans het achtervoegsel [!DNL .icc] of [!DNL .icm] en bevinden zich op dezelfde locatie als materiaalgegevensbestanden.

Hoewel uitvoerprofielen kunnen worden opgegeven op bestandspad/-naam in de opdracht `icc=`, wordt aangeraden alle profielbestanden te registreren in de ICC-profielkaart van de standaardcatalogus of in een specifieke materiaalcatalogus en sneltoetsidentificatoren ( `icc::Name`) te gebruiken in plaats van bestandspaden.

Werkprofielen moeten worden geregistreerd in de ICC-profielkaart van de materiaalcatalogus of de standaardcatalogus.
