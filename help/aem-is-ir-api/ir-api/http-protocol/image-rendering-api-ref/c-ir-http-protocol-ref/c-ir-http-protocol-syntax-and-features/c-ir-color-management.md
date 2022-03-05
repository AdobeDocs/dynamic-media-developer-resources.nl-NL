---
description: Rendering van afbeeldingen ondersteunt kleurruimteconversies op basis van kleurruimteprofielen die voldoen aan de ICC-specificatie (International Color Consortium).
solution: Experience Manager
title: Kleurbeheer voor rendering van afbeeldingen *
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa772ab2-8a32-4c1a-9ee3-c1cf4a0b3095
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '736'
ht-degree: 0%

---

# Kleurbeheer voor rendering van afbeeldingen *{#image-rendering-color-management}

Rendering van afbeeldingen ondersteunt kleurruimteconversies op basis van kleurruimteprofielen die voldoen aan de ICC-specificatie (International Color Consortium).

**Beperkingen**

Momenteel worden alleen CMYK-, RGB- en grijswaardenkleurruimten ondersteund.

Stijlbestanden voor kabinetsopmaakbestanden (.vnc) en vensterbekledingsbestanden ( [!DNL .vnw]) niet worden beheerd en worden verondersteld te bestaan in de werkkleurruimte.

**Zie ook**

[International Color Consortium](https://www.color.org/index.xalter) , [ `icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06) , [ `iccEmbed=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f) , `attribute::IccProfile*` , `attribute::IccProfileSrc*`, `attribute::IccRenderIntent` , `attribute::IccBlackPointCompensation` , `attribute::IccDither` , ICC-profielkaarten

## Standaardkleurruimten {#section-8ce27edf42e746febe4654f8f19b9c0c}

Elke afbeeldingscatalogus (en de standaardcatalogus) kunnen een set ICC-profielen definiëren. Deze profielen vormen de standaardkleurruimten voor deze catalogus: één invoer- en één uitvoerprofiel voor elk grijswaarden-, RGB- en CMYK-gegevens ( `attribute::IccProfileRgb`, `attribute::IccProfileGray`, `attribute::IccProfileCmyk`, `attribute::IccProfileSrcRgb`, `attribute::IccProfileSrcGray`, en `attribute::IccProfileSrcCmyk`).

De standaardkleurruimte voor een bepaalde afbeelding of een ander object wordt geselecteerd in de standaardprofielen van de catalogus op basis van het pixeltype van de afbeelding.

## Invoerkleurruimte {#section-660f661a7e954df4b451e34134195276}

Materiële afbeeldingen kunnen ICC-profielen insluiten om de invoerkleurruimte te definiëren. Als er geen profiel is ingesloten in een bronafbeelding, `attribute::IccProfileSrc*` van de toepasselijke afbeeldingscatalogus wordt gebruikt die overeenkomt met het pixeltype van de bronafbeelding. Als dit kenmerk niet is gedefinieerd in de afbeeldingscatalogus, `attribute::IccProfile*` wordt gebruikt. Als dat cataloguskenmerk ook niet is gedefinieerd, wordt de afbeelding niet in kleur beheerd en worden alleen naïeve transformaties toegepast.

## Werkkleurruimte {#section-645d9cfa5b0347a190a0ece218f5b5e1}

De werkkleurruimte wordt meestal gedefinieerd door het ICC-kleurprofiel dat is ingesloten in het vignet. Als het vignet geen profiel bevat, wordt het standaard RGB-invoerprofiel ( `attribute::IccProfileSrcRgb` van de sessiecatalogus) wordt gebruikt voor de werkkleurruimte.

Alle renderbewerkingen worden uitgevoerd in de werkkleurruimte.

**Belangrijk:** Het ICC-profiel voor de werkkleurruimte moet invoer- en uitvoertransformaties ondersteunen. Als een alleen-uitvoerprofiel wordt gebruikt als werkkleurruimte, kan AIR materialen niet omzetten in een profiel. Een dergelijk kleurprofiel kan nog steeds worden gebruikt als de materialen zich in dezelfde werkkleurruimte bevinden. Het toepassen van materialen in andere kleurruimten mislukt.

## Expliciete kleurwaarden {#section-31727bf1b23e477ca92572fbbf422d2f}

RGB-kleurwaarden opgegeven met `color=`, `bgc=`, `catalog::BgColor`, en `catalog::Color` worden verondersteld te bestaan in de huidige werkkleurruimte.

## Materiaalgegevensbestanden {#section-33f7a170a6664c02b8479fb89cc0aea3}

Materiaalafbeeldingsbestanden (structuur- en decale afbeeldingen) kunnen van het type RGB, grijswaarden of CMYK-pixels zijn en kunnen een kleurprofiel insluiten. Als er geen kleurprofiel is ingesloten, wordt de standaardinvoerkleurruimte aan de afbeelding gekoppeld (bijvoorbeeld het kleurprofiel uit de materiaalcatalogus dat overeenkomt met het pixeltype van de afbeelding).

Materiaalafbeeldingen die worden verkregen bij verzoeken om geneste afbeeldingsserver of om het renderen van afbeeldingen, bevatten doorgaans een kleurprofiel. Als dit niet het geval is, worden de afbeeldingen gekoppeld aan de standaardinvoerkleurruimte die overeenkomt met het pixeltype.

Als de kleurruimte van het afbeeldingsbestand anders is dan de werkkleurruimte, wordt een nauwkeurige kleuromzetting gebruikt om de afbeelding om te zetten in de werkkleurruimte. Typeconversie van het type naïef wordt gebruikt wanneer geen profiel wordt ingebed en geen standaard inputprofiel wordt bepaald.

Andere materiaalgegevensbestanden, zoals bestanden in kabinetstijl ( [!DNL .vnc]) of venster dat bestanden bedekt ( [!DNL .vnw]) kleurprofielen niet insluiten en altijd wordt aangenomen dat deze zich in de werkkleurruimte bevinden.

## Uitvoerkleurruimte {#section-4c2c4dfedbb8429ba5cfddc3d3eab6c4}

Alle renderbewerkingen vinden plaats in de werkkleurruimte. Als in de aanvraag een ander kleurprofiel wordt opgegeven met de `icc=` worden de gegevens naar die kleurruimte geconverteerd vlak voordat deze worden gecodeerd en aan de client worden geretourneerd. Als kleurbeheer is uitgeschakeld, wordt indien nodig naïeve omzetting gebruikt om de afbeelding om te zetten in grijswaarden of CMYK.

## Ingesloten kleurprofielen {#section-5ff733832d38429fbe02b3c1e9bb94a9}

Het kleurprofiel dat aan de gerenderde afbeelding is gekoppeld, kan in de reactieafbeelding worden ingesloten door `iccEmbed=` voor het verzoek.

Indien `icc=` niet is opgegeven, wordt het ICC-profiel voor de werkkleurruimte ingesloten. Er is geen profiel ingesloten als kleurbeheer is uitgeschakeld en er geen profiel is opgegeven met `icc=`.

## ICC-profielen {#section-afeb76068b5042adb83261638e450140}

Alle kleurprofielen die door de server worden gebruikt, moeten voldoen aan de ICC-specificatie. ICC-profielbestanden hebben doorgaans een [!DNL .icc] of [!DNL .icm] bestandsachtervoegsel en bevinden zich op dezelfde locatie als de materiaalgegevensbestanden.

Uitvoerprofielen kunnen op bestandspad/naam worden opgegeven in het dialoogvenster `icc=` wordt aangeraden alle profielbestanden te registreren in de ICC-profielkaart van de standaardcatalogus of een specifieke materiaalcatalogus en sneltoetsidentificatoren te gebruiken ( `icc::Name`) in plaats van bestandspaden.

Werkprofielen moeten worden geregistreerd in de ICC-profielkaart van de materiaalcatalogus of de standaardcatalogus.
