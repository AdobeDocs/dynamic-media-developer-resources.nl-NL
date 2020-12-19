---
description: Vignetten zijn afbeeldingen die zijn ontworpen met Scene7 Image Authoring voor gebruik met behulp van Image Rendering.
seo-description: Vignetten zijn afbeeldingen die zijn ontworpen met Scene7 Image Authoring voor gebruik met behulp van Image Rendering.
seo-title: Vignetten
solution: Experience Manager
title: Vignetten
topic: Scene7 Image Serving - Image Rendering API
uuid: 31d6b2b7-57c4-4fef-a498-c357c3724356
translation-type: tm+mt
source-git-commit: 7721cccf3f779f258adcdcf886f7e01111e92be0
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 0%

---


# Vignetten{#vignettes}

Vignetten zijn afbeeldingen die zijn ontworpen met Scene7 Image Authoring voor gebruik met behulp van Image Rendering.

IR ondersteunt twee basistypen vignetten, *2D* en *3D*. De scènes van de ruimte zijn typisch 3D vignetten die reflecties kunnen teruggeven, terwijl de meeste andere scènes, zoals kleding of stoffering, normaal 2D vignetten zijn die reflectie het teruggeven vermogen niet hebben.

Vignetten bevatten een *view* en een hiërarchie van *objecten*.

De weergave is de container voor de hoofdafbeelding, gedeelde verlichtingstoewijzingen, gedeelde spiegelingstoewijzingen en andere gegevens die aan de gehele afbeelding zijn gekoppeld.

De objecthiërarchie bestaat uit *objectgroepen*, *standaardobjecten* en *overlappen objecten*.

Elk standaardobject bestuurt een gebied van de weergaveafbeelding, gedefinieerd met een grijsschaal *mask*. De maskers van standaardobjecten overlappen elkaar nooit. Standaardobjecten kunnen niet rechtstreeks worden verborgen, maar kunnen gedeeltelijk of geheel door overlappende objecten worden bedekt. De meeste of alle objecten in een normaal vignet zijn standaardobjecten.

Objecten overlappen elkaar boven op de weergaveafbeelding. De overlappende volgorde wordt gedefinieerd door een z-waarde die aan het object is toegewezen. Objecten overlappen is handig wanneer delen van een scène dynamisch moeten worden weergegeven of verborgen.

Verschillende typen objecten worden ondersteund (zowel standaard als overlappend), waarbij elk object een eigen specifieke functie heeft:

* **Vlakke objecten**  (in 3D-vignetten) en  **vlakke objecten**  (in 2D-vignetten) accepteren herhaalbare structuurmaterialen. Deze worden doorgaans gebruikt voor vloeren, tegenoverstellingen en andere vlakke oppervlakken waarvoor alleen perspectieftoewijzing is vereist.

* **Stroomlijningsobjecten** geven vloeiend gevormde gekromde oppervlakken, zoals stoffering, toe en worden soms ook gebruikt voor kleurobjecten. Ze kunnen zowel in 2D- als in 3D-vignetten worden gebruikt en, als ze volledig zijn ontworpen, nemen deel aan rendering van reflecties.
* **Niet-tekstuele** objecten staan alleen kleurverschuivingen toe. Ze zijn toegestaan in zowel 2D- als 3D-vignetten. Ze zijn inherent niet-tekstueel of kunnen een vlak- of stroomlijnobject zijn met een speciale markering &#39;Geen structuur&#39; ingesteld. Dit is handig in 3D-vignetten om objecten toe te staan deel te nemen aan rendering van spiegelingen, ook al accepteert het object alleen effen kleurmaterialen.
* **Schetsobjecten** kunnen het beste worden gebruikt voor stof-objecten met vouwen en rimpels, zoals kleding. Net als stroomlijnobjecten kunnen ze worden gebruikt in 2D- en 3D-vignetten, hoewel de toepassing in 3D-vignetten beperkt is.
* **Muur-** objecten lijken op vlakke objecten en worden alleen ondersteund in 3D-vignetten. Zij hebben speciale lay-outinformatie die toepassing van twee verschillende muurafwerking (hoger en lager) en tot drie materialen van de muurgrens toestaat. Wanneer correct ontworpen, zullen de materialen die op muren worden toegepast nauwkeurig en naadloos tussen aangrenzende muren, voor realistische achtergrond/muurgrenstoepassingen stromen. Muurobjecten ondersteunen structuurrotatie niet.
* **Cabinet-** objecten zijn alleen toegestaan in 3D-vignetten. Ze worden gebruikt om keuken- en badkuipen met complexe layoutvereisten te maken. Cabinet-objecten accepteren herhaalbare structuren en speciaal ontworpen *kabinetsstijlbestanden* die resizable kabinetsdeelafbeeldingen bevatten.

Naast de basisobjecttypen worden twee speciale soorten overlappende objecten ondersteund:

* **Statische overlappende** objecten zijn objecten die geen materialen accepteren. Ze zijn toegestaan in zowel 2D- als 3D-vignetten. Ze zijn handig voor verwijderbare accessoires in een kamerscène, voor slagschaduwen achter renderbare overlappende objecten en vergelijkbare toepassingen.
* **Venster dat frameobjecten bedekt,** biedt plaatsingsinformatie voor het toepassen van Window coverings-stijlbestanden, die onafhankelijk van het vignet zijn ontworpen en onder vignetten kunnen worden gedeeld.

Objecten worden verzameld in *objectgroepen*, vergelijkbaar met een bestandssysteem. Groepering is gewoonlijk gebaseerd op de structuur van de fysieke objecten die zij vertegenwoordigen (een groep &quot;Alle kasten&quot; kan bijvoorbeeld &quot;Basiskasten&quot; en &quot;Muurkasten&quot; bevatten). Een willekeurig aantal groepsniveaus is toegestaan. Groeperen ondersteunt de toepassing van materialen op meerdere, vergelijkbare objecten.

* [Scènecoördinaten](c-ir-scene-coordinates.md)
* [Materiaalresolutie](c-ir-material-resolution.md)
