---
description: De afbeelding die naar de client wordt geretourneerd als reactie op een aanvraag req=tmb, wordt afgeleid van de samengestelde afbeelding door de volgende waarden wid=, hei=, attribute DefaultThumbPix en attribute MaxPix in overweging te nemen.
solution: Experience Manager
title: Transformatie weergeven voor miniaturen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7db6736f-0b49-4c4f-89c5-e89d4752f339
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# Transformatie weergeven voor miniaturen{#view-transform-for-thumbnails}

De afbeelding die naar de client wordt geretourneerd als reactie op een aanvraag req=tmb, wordt afgeleid van de samengestelde afbeelding op basis van de volgende waarden: wid=, hei=, attribute::DefaultThumbPix, and attribute::MaxPix.

1. **De weergaverechthoek berekenen** - Gebruik `wid=` of de breedtewaarde van `attribute::DefaultThumbPix` voor de breedte van de weergaverechthoek. Gebruiken `hei=` of de hoogtewaarde van `attribute::DefaultThumbPix` voor de hoogte. Het weergaverect moet in deze stap volledig worden opgegeven. (De weergave-rect is gelijk aan de laag 0 rect, als dit niet het geval is `size=`wordt opgegeven voor laag 0).
1. **De samenstelling schalen** - Indien `catalog::ThumbType=Crop`, wordt de samenstelling geschaald tot het kleinst mogelijke beeld terwijl nog het volledige meningsrect vult; extra afbeeldingsgegevens worden uitgeschakeld. Indien `catalog::ThumbType= Fit`Vervolgens wordt de samenstelling geschaald naar het grootst mogelijke beeld, terwijl de volledige samengestelde afbeelding nog steeds in het weergaverect past. Indien `catalog::ThumbType=Texture`, wordt de samenstelling helemaal niet geschaald om de resolutie te behouden die is opgegeven in `catalog::ThumbRes`.
1. **Vullen en uitsnijden** - De weergaverechthoek is gevuld met de `bgc=` kleur (of, indien niet opgegeven, met `attribute::ThumbBkgColor`). De geschaalde samengestelde afbeelding wordt uitgelijnd met het kenmerk view rect: `ThumbHorizAlign` en kenmerk: `ThumbVertAlign`. De geschaalde samenstelling wordt vervolgens zonder verdere schaling samengevoegd met de gevulde weergaverechthoek. Alle gebieden van de samenstelling die buiten de weergaverechthoek vallen, worden uitgeschakeld.
