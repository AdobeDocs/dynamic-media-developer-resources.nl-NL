---
description: De afbeelding die naar de client wordt geretourneerd als reactie op een aanvraag req=tmb, wordt afgeleid van de samengestelde afbeelding door de volgende waarden wid=, hei=, attribute DefaultThumbPix en attribute MaxPix in overweging te nemen.
seo-description: De afbeelding die naar de client wordt geretourneerd als reactie op een aanvraag req=tmb, wordt afgeleid van de samengestelde afbeelding door de volgende waarden wid=, hei=, attribute DefaultThumbPix en attribute MaxPix in overweging te nemen.
seo-title: Transformatie weergeven voor miniaturen
solution: Experience Manager
title: Transformatie weergeven voor miniaturen
topic: Scene7 Image Serving - Image Rendering API
uuid: 29924bc1-ada1-420f-aef7-bf9a7db7065b
translation-type: tm+mt
source-git-commit: aa095022d43db4bf815aece9bc2b087c53a64e1b

---


# Transformatie weergeven voor miniaturen{#view-transform-for-thumbnails}

De afbeelding die naar de client wordt geretourneerd als reactie op een aanvraag req=tmb, wordt afgeleid van de samengestelde afbeelding op basis van de volgende waarden: wid=, hei=, attribute::DefaultThumbPix, and attribute::MaxPix.

1. **Bereken de weergaverechthoek** - Gebruik `wid=` of de breedtewaarde van `attribute::DefaultThumbPix` voor de breedte van de weergaverechthoek. Gebruik `hei=` of de hoogtewaarde van `attribute::DefaultThumbPix` voor de hoogte. Het weergaverect moet in deze stap volledig worden opgegeven. (De weergaverechthoek komt overeen met de rechthoek van laag 0 als er geen waarde `size=`is opgegeven voor laag 0).
1. **De samenstelling** schalen - Als `catalog::ThumbType=Crop`, dan wordt de samenstelling geschraapt aan het kleinst mogelijke beeld terwijl het vullen van het volledige meningsrect; extra afbeeldingsgegevens worden uitgeschakeld. Als `catalog::ThumbType= Fit`, dan wordt de samenstelling geschraapt aan het grootste mogelijke beeld terwijl nog het passen van de volledige samenstelling in de meningsrect. Als `catalog::ThumbType=Texture`de samenstelling überhaupt niet wordt geschaald om de resolutie te behouden die in `catalog::ThumbRes`.
1. **Vulling en uitsnijden** - Het weergavevak wordt gevuld met de `bgc=` kleur (of, indien niet opgegeven, met `attribute::ThumbBkgColor`). De geschaalde samengestelde afbeelding wordt uitgelijnd met het kenmerk view rect: `ThumbHorizAlign` en kenmerk: `ThumbVertAlign`. De geschaalde samenstelling wordt vervolgens zonder verdere schaling samengevoegd met de gevulde weergaverechthoek. Alle gebieden van de samenstelling die buiten de weergaverechthoek vallen, worden uitgeschakeld.

