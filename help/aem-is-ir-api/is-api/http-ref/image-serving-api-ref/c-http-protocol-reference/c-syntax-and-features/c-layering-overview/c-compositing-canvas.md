---
description: Lagen worden samengesteld in de volgorde die is opgegeven met de opdracht layer=, waarbij hoger genummerde lagen lager genummerde lagen verbergen.
seo-description: Lagen worden samengesteld in de volgorde die is opgegeven met de opdracht layer=, waarbij hoger genummerde lagen lager genummerde lagen verbergen.
seo-title: Het samengestelde canvas
solution: Experience Manager
title: Het samengestelde canvas
topic: Scene7 Image Serving - Image Rendering API
uuid: 057b11cb-36f3-40f8-b095-9ad05da858a9
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---


# Het samengestelde canvas{#the-compositing-canvas}

Lagen worden samengesteld in de volgorde die is opgegeven met de opdracht layer=, waarbij hoger genummerde lagen lager genummerde lagen verbergen.

Laag 0 vormt de achtergrondlaag, die altijd wordt vereist en die de grootte van het samengestelde beeld bepaalt. Alle laagtypen zijn toegestaan voor laag 0. De grootte van laag 0 moet worden gedefinieerd, waarbij expliciet `size=` of impliciet wordt gebruikt, op basis van de afbeelding of tekst van de inhoud. Gebieden van andere lagen die buiten het gebied van laag 0 vallen, worden niet opgenomen in de uitvoerafbeelding.

>[!NOTE]
>
>Nadat alle lagen zijn afgevlakt, wordt het samengestelde beeld omgezet in het definitieve reactiebeeld, zoals gespecificeerd met [meningsbevelen en attributen](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90).

