---
description: In dit voorbeeld wordt Afbeeldingsserver gebruikt om een object te vullen met kleur en een decal toe te passen dat aangepaste tekst bevat in een van de vignetten.
seo-description: In dit voorbeeld wordt Afbeeldingsserver gebruikt om een object te vullen met kleur en een decal toe te passen dat aangepaste tekst bevat in een van de vignetten.
seo-title: Voorbeelden
solution: Experience Manager
title: Voorbeelden
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9f8e4346-6efe-4f21-982d-613328bd708d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 0%

---


# Voorbeelden{#examples}

In dit voorbeeld wordt Afbeeldingsserver gebruikt om een object te vullen met kleur en een decal toe te passen dat aangepaste tekst bevat in een van de vignetten.

AIR-variabelen worden gebruikt om het vignet, de logoafbeelding en de aangepaste tekst te identificeren.

Het veld `vignette::Modifier` in de record *template* in de vignetkaart van de materiaalcatalogus `myCat` bevat het volgende:

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

Alle vignetten die worden gebruikt, worden vermeld in het vignetoverzicht van de materiaalcatalogus `myCat`.

De client kan nu het volgende verzoek indienen om de standaardafbeelding op te halen (hierbij worden de variabelen gebruikt die aan het begin van de sjabloon zijn gedefinieerd):

[!DNL `https://server/myCat/template`]

In het volgende verzoek wordt bepaalde inhoud opgegeven die moet worden gerenderd:

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

Raadpleeg de documentatie bij Beeldserver voor meer informatie over de opdracht Beeldwerking `text=`.
