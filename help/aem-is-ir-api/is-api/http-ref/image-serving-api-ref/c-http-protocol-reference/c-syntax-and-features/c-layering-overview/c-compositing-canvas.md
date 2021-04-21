---
description: Lagen worden samengesteld in de volgorde die is opgegeven met de opdracht layer=, waarbij hoger genummerde lagen lager genummerde lagen verbergen.
solution: Experience Manager
title: Het samengestelde canvas
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# Het samengestelde canvas{#the-compositing-canvas}

Lagen worden samengesteld in de volgorde die is opgegeven met de opdracht layer=, waarbij hoger genummerde lagen lager genummerde lagen verbergen.

Laag 0 vormt de achtergrondlaag, die altijd wordt vereist en die de grootte van het samengestelde beeld bepaalt. Alle laagtypen zijn toegestaan voor laag 0. De grootte van laag 0 moet worden gedefinieerd, waarbij expliciet `size=` of impliciet wordt gebruikt, op basis van de afbeelding of tekst van de inhoud. Gebieden van andere lagen die buiten het gebied van laag 0 vallen, worden niet opgenomen in de uitvoerafbeelding.

>[!NOTE]
>
>Nadat alle lagen zijn afgevlakt, wordt het samengestelde beeld omgezet in het definitieve reactiebeeld, zoals gespecificeerd met [meningsbevelen en attributen](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90).

