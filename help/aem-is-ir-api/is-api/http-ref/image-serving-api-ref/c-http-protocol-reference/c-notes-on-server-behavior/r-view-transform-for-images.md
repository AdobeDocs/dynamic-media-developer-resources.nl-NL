---
description: Transformatie weergeven voor afbeeldingen
solution: Experience Manager
title: Transformatie weergeven voor afbeeldingen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fc20cbc2-9d66-4c52-80c2-9ba7c3b54744
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# Transformatie weergeven voor afbeeldingen{#view-transform-for-images}

De afbeelding die als reactie op een `req=img` Het verzoek wordt afgeleid van het samengestelde beeld door de volgende waarden te overwegen: `wid=`, `hei=`, `fit=`, `scl=`, `rgn=`, `attribute::DefaultPix`, `attribute::MaxPix`en de grootte van de samengestelde afbeelding.

Indien `wid=` en `hei=` gespecificeerd zijn, en `scl=` is niet, wordt de samengestelde afbeelding geschaald zodat deze volledig past binnen de weergaverechthoek die wordt gedefinieerd door `wid=` en `hei=`. Als de hoogte-breedteverhouding van de weergaverechthoek verschilt van die van de samengestelde afbeelding, wordt de geschaalde samengestelde afbeelding binnen de weergaverechthoek uitgelijnd met de `align=` waarde, indien opgegeven, of anders gecentreerd. Elke ruimte die niet door afbeeldingsgegevens wordt gedekt, wordt gevuld met `bgc=` of, indien niet gespecificeerd, met `attribute::BkgColor`.

Indien `scl=` wordt opgegeven, wordt de samengestelde afbeelding met die schaalfactor geschaald. Indien `wid=` en/of `hei=` wordt ook opgegeven, wordt de geschaalde afbeelding vervolgens uitgesneden tot `wid=` en/of `hei=` of er wordt, indien nodig, extra ruimte toegevoegd. `align=` Hiermee geeft u aan waar de afbeelding wordt uitgesneden of extra ruimte wordt toegevoegd en eventuele extra ruimte wordt gevuld met `bgc=` of `attribute::BkgColor`.

Als beide `wid=`, `hei=` noch `scl=` worden opgegeven en als een breedte of hoogte van de samengestelde afbeelding groter is dan `attribute::DefaultPix`en wordt de samengestelde afbeelding geschaald tot maximaal `attribute::DefaultPix`. Anders wordt de samengestelde afbeelding gebruikt zonder te schalen.

Om ervoor te zorgen dat de weergaveafbeelding wordt geretourneerd zonder verdere schaling, geeft u `scl=1`.

Indien `rgn=` wordt opgegeven, wordt de antwoordafbeelding vervolgens bijgesneden om de uiteindelijke afbeeldingsgrootte van de reactie te verkrijgen. Deze grootte wordt vergeleken met `attribute::MaxPix` (indien gedefinieerd) en er wordt een fout gegenereerd als de antwoordafbeelding groter is in een van beide dimensies.

Indien `fmt=` geeft gegevens zonder alfa aan, alle transparante gebieden in de antwoordafbeelding worden gevuld met `bgc=` of `attribute::BkgColor`.
