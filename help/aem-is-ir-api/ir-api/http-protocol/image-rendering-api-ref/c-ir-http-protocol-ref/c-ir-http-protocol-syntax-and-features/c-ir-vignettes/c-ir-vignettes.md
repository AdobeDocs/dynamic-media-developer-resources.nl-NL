---
title: Vignetten
description: Vignetten zijn afbeeldingen die zijn ontworpen met Dynamic Media Image Authoring voor gebruik met behulp van Image Rendering.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5e1be99c-58c0-4e3c-bc57-7be5fa25ccef
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 0%

---

# Vignetten{#vignettes}

Vignetten zijn afbeeldingen die zijn ontworpen met Dynamic Media Image Authoring voor gebruik met behulp van Image Rendering.

IR steunt twee basistypes vignetten: *2D* en *3D*. Kamerscènes zijn doorgaans 3D-vignetten die reflecties kunnen renderen, terwijl de meeste andere scènes, zoals kleding of stoffering, normaal gesproken 2D-vignetten zijn die geen reflectie-renderfunctie hebben.

Vignetten bevatten een *weergave* en een hiërarchie van *objecten*.

De weergave is de container voor de hoofdafbeelding, gedeelde verlichtingstoewijzingen, gedeelde spiegelingstoewijzingen en andere gegevens die aan de gehele afbeelding zijn gekoppeld.

De objecthiërarchie bestaat uit *objectgroepen*, *standaardobjecten*, en *overlappen, objecten*.

Elk standaardobject bestuurt een gebied van de weergaveafbeelding, gedefinieerd met een grijswaarden *masker*. De maskers van standaardobjecten overlappen elkaar nooit. Standaardobjecten kunnen niet rechtstreeks worden verborgen, maar kunnen gedeeltelijk of geheel door overlappende objecten worden bedekt. De meeste of alle objecten in een normaal vignet zijn standaardobjecten.

Objecten overlappen elkaar boven op de weergaveafbeelding. De overlappende volgorde wordt gedefinieerd door een z-waarde die aan het object is toegewezen. Objecten overlappen zijn handig wanneer delen van een scène dynamisch moeten worden weergegeven of verborgen.

Verschillende typen objecten worden ondersteund (zowel standaard als overlappend), waarbij elk object een eigen specifieke functie heeft:

* **Vlakke objecten** (in 3D-vignetten) en **vlakke objecten** (in 2D-vignetten) kunt u gebruikmaken van herhaalbare structuurmaterialen. Deze worden doorgaans gebruikt voor vloeren, tegenoverstellingen en andere vlakke oppervlakken waarvoor alleen perspectieftoewijzing is vereist.
* **Stroomlijnde objecten** Hiermee kunt u vloeiend gevormde gebogen oppervlakken, zoals stoffering, toewijzen. Deze worden soms ook gebruikt voor kleurobjecten. Ze kunnen zowel in 2D- als in 3D-vignetten worden gebruikt en, als ze volledig zijn ontworpen, deelnemen aan rendering van weerspiegelingen.
* **Niet-tekstuele objecten** alleen kleurverschuivingen toestaan. Ze zijn toegestaan in zowel 2D- als 3D-vignetten. Ze zijn inherent niet-tekstueel of kunnen een vlak- of stroomlijnobject zijn met een speciale markering &#39;Geen structuur&#39; ingesteld. Deze methode is handig in 3D-vignetten om objecten toe te staan deel te nemen aan rendering van spiegelingen, ook al accepteert het object alleen effen kleurmaterialen.
* **Schetsobjecten** Deze filters kunnen het beste worden gebruikt voor weefsels met vouwen en rimpels, zoals kledingstukken. Net als stroomlijnobjecten kunnen ze worden gebruikt in 2D- en 3D-vignetten, hoewel de toepassing in 3D-vignetten beperkt is.
* **Muurobjecten** lijken op vlakke objecten en worden alleen ondersteund in 3D-vignetten. Zij hebben speciale lay-outinformatie die toepassing van twee verschillende muurafwerking (hoger en lager) en tot drie materialen van de muurgrens toestaat. Wanneer correct ontworpen, stromen de materialen die op muren worden toegepast nauwkeurig en naadloos tussen aangrenzende muren, voor realistische achtergrond/muurgrenstoepassingen. Muurobjecten ondersteunen structuurrotatie niet.
* **Kabinetsobjecten** zijn alleen toegestaan in 3D-vignetten. Ze worden gebruikt om keuken- en badkuipen met complexe layoutvereisten te maken. Cabinet-objecten accepteren herhaalbare structuren en speciaal ontworpen *kabinetsstijlbestanden* met verstelbare paneelafbeeldingen voor het kabinet.

Naast de basisobjecttypen worden twee speciale soorten overlappende objecten ondersteund:

* **Statische overlappende objecten** zijn objecten die geen materialen accepteren. Ze zijn toegestaan in zowel 2D- als 3D-vignetten. Ze zijn handig voor verwijderbare accessoires in een kamerscène, voor slagschaduwen achter renderbare overlappende objecten en vergelijkbare toepassingen.
* **Venster dat frameobjecten bedekt** Geef plaatsingsinformatie voor het toepassen van de stijlbestanden van vensterbekledingen, die onafhankelijk van het vignet zijn ontworpen en onder vignetten kunnen worden gedeeld.

Objecten worden verzameld in *objectgroepen*, vergelijkbaar met een bestandssysteem. Groepering is gewoonlijk gebaseerd op de structuur van de fysieke objecten die zij vertegenwoordigen (een groep &#39;Alle kasten&#39; kan bijvoorbeeld &#39;Basiskasten&#39; en &#39;Muurkasten&#39; bevatten). Een willekeurig aantal groepsniveaus is toegestaan. Groeperen ondersteunt de toepassing van materialen op meerdere, vergelijkbare objecten.

* [Scènecoördinaten](c-ir-scene-coordinates.md)
* [Materiaalresolutie](c-ir-material-resolution.md)
