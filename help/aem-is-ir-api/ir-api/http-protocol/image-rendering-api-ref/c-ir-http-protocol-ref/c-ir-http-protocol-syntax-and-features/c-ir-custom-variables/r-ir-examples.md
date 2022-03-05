---
title: Voorbeelden
description: In dit voorbeeld wordt Afbeeldingsserver gebruikt om een object te vullen met kleur en een decal toe te passen dat aangepaste tekst bevat in een van de vignetten.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 85f11642-e1ff-4bf0-bd21-d419805cff4a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# Voorbeelden{#examples}

In dit voorbeeld wordt Afbeeldingsserver gebruikt om een object te vullen met kleur en een decal toe te passen dat aangepaste tekst bevat in een van de vignetten.

AIR-variabelen worden gebruikt om het vignet, de logoafbeelding en de aangepaste tekst te identificeren.

De `vignette::Modifier` veld in de record met de naam *template* in de vignetkaart van de materiaalcatalogus `myCat` bevat het volgende:

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

Alle gebruikte vignetten worden vermeld in de vignetkaart van de materiaalcatalogus `myCat`.

De client kan nu het volgende verzoek indienen om de standaardafbeelding op te halen (gebruikt de variabelen die aan het begin van de sjabloon zijn gedefinieerd):

[!DNL `https://server/myCat/template`]

In het volgende verzoek wordt bepaalde inhoud opgegeven die moet worden gerenderd:

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

Raadpleeg de documentatie bij Beeldserver voor meer informatie over de beeldserver `text=` gebruiken.
