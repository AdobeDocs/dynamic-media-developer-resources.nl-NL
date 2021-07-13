---
description: De afbeelding die naar de client wordt geretourneerd als reactie op een aanvraag req=tmb, wordt afgeleid van de samengestelde afbeelding door de volgende waarden wid=, hei=, attribute DefaultThumbPix en attribute MaxPix in overweging te nemen.
solution: Experience Manager
title: Transformatie weergeven voor miniaturen
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 7db6736f-0b49-4c4f-89c5-e89d4752f339
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Transformatie weergeven voor miniaturen{#view-transform-for-thumbnails}

De afbeelding die naar de client wordt geretourneerd als reactie op een aanvraag req=tmb, wordt afgeleid van de samengestelde afbeelding op basis van de volgende waarden: wid=, hei=, attribute::DefaultThumbPix, and attribute::MaxPix.

1. **Bereken de weergaverechthoek** : gebruik  `wid=` of de breedtewaarde van  `attribute::DefaultThumbPix` voor de breedte van de weergaverechthoek. Gebruik `hei=` of de hoogtewaarde van `attribute::DefaultThumbPix` voor de hoogte. Het weergaverect moet in deze stap volledig worden opgegeven. (De weergaverechthoek zal gelijk zijn aan de laag 0 rect, als er geen `size=`is opgegeven voor laag 0).
1. **De samenstelling**  schalen - Als  `catalog::ThumbType=Crop`, dan wordt de samenstelling geschraapt aan het kleinst mogelijke beeld terwijl nog het volledige meningsrect vult; extra afbeeldingsgegevens worden uitgeschakeld. Als `catalog::ThumbType= Fit`, dan wordt de samenstelling geschraapt aan het grootste mogelijke beeld terwijl nog het passen van de volledige samenstelling in de meningsrect. Als `catalog::ThumbType=Texture`, wordt de samenstelling niet geschaald om de resolutie te bewaren die in `catalog::ThumbRes` wordt gespecificeerd.
1. **Vulling en uitsnijden**  - Het weergavevak wordt gevuld met de  `bgc=` kleur (of, indien niet opgegeven, met  `attribute::ThumbBkgColor`). De geschaalde samengestelde afbeelding wordt uitgelijnd met het kenmerk view rect: `ThumbHorizAlign` en kenmerk: `ThumbVertAlign`. De geschaalde samenstelling wordt vervolgens zonder verdere schaling samengevoegd met de gevulde weergaverechthoek. Alle gebieden van de samenstelling die buiten de weergaverechthoek vallen, worden uitgeschakeld.
