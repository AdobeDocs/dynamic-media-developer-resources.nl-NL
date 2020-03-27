---
description: Als u een afbeelding wilt bewerken, kunt u referentiepunten gebruiken die vergelijkbaar zijn met kompaspunten.
seo-description: Als u een afbeelding wilt bewerken, kunt u referentiepunten gebruiken die vergelijkbaar zijn met kompaspunten.
seo-title: FXG-serverprotocol
solution: Experience Manager
title: FXG-serverprotocol
topic: Scene7 Image Serving - Image Rendering API
uuid: 5cb123ca-2274-4ddb-8fa1-ab22a19172f6
translation-type: tm+mt
source-git-commit: 26fb6212c3106deb7b088020d9f2993e40dec20b

---


# FXG-serverprotocol{#fxg-server-protocol}

Als u een afbeelding wilt bewerken, kunt u referentiepunten gebruiken die vergelijkbaar zijn met kompaspunten.

Met behulp van referentiepunten kunt u een afbeelding roteren, schalen of de grootte ervan wijzigen ten opzichte van een bepaald referentiepunt. De referentiepunten zijn `northWest`, `north`, `northEast`, `west`, `center`, `east`, `southWest`, `south`, en `southeast`. Als u bijvoorbeeld het middelste referentiepunt gebruikt, kunt u een afbeelding in het midden 45 graden draaien. In deze afbeelding ziet u waar de referentiepunten zich bevinden, een afbeelding, de afbeelding 20 graden gedraaid ten opzichte van het `northWest` referentiepunt en de afbeelding 20 graden gedraaid ten opzichte van het `east` referentiepunt.

![](assets/wp_ref_points.png)

* A. Locatie referentiepunt
* B. Een afbeelding
* C. De afbeelding is 20 graden gedraaid ten opzichte van het `northWest` referentiepunt
* D. De afbeelding is 20 graden gedraaid ten opzichte van het `east` referentiepunt

De syntaxis is:

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

De standaardwaarde is geen. De `inherit` waarde geeft de `s7:referencePoint` `none`waarde, op voorwaarde dat dit niet het geval is, van de bovenkant van de pagina of het groepsniveau door aan alle onderliggende items. De `none` instelling betekent dat er geen referentiepunt is voor het object en dat het FXG-coördinatensysteem wordt gebruikt.

>[!NOTE]
>
>Als u een referentiepunt wilt gebruiken en geen verschuiving in het object wilt toepassen nadat het is gemanipuleerd, werkt u de x- en y-waarden van het object bij nadat u het hebt bewerkt.

Wanneer een waarde uit `s7:referencePoint` wordt gebruikt met groepen (of paden, lijnelementen of elementen zonder expliciete breedte- en hoogtedefinities), wordt de waarde toegepast op het cumulatieve selectiekader van de groep. Het punt linksboven van het selectiekader van alle objecten in de groep fungeert bijvoorbeeld als `northWest` referentiepunt voor de groep; het punt rechtsonder fungeert als `southEast` referentiepunt.

