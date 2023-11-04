---
description: Lagen worden samengesteld in de volgorde die is opgegeven met de opdracht layer=, waarbij hoger genummerde lagen lager genummerde lagen verbergen.
solution: Experience Manager
title: Het samengestelde canvas
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2455d07f-a158-4335-a14c-213f8b3dd265
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# Het samengestelde canvas{#the-compositing-canvas}

Lagen worden samengesteld in de volgorde die is opgegeven met de opdracht layer=, waarbij hoger genummerde lagen lager genummerde lagen verbergen.

Laag 0 vormt de achtergrondlaag, die altijd wordt vereist en die de grootte van het samengestelde beeld bepaalt. Alle laagtypen zijn toegestaan voor laag 0. De grootte van laag 0 moet worden bepaald, of uitdrukkelijk gebruikend `size=` of impliciet, gebaseerd op de inhoudsafbeelding of tekst. Gebieden van andere lagen die buiten het gebied van laag 0 vallen, worden niet opgenomen in de uitvoerafbeelding.

>[!NOTE]
>
>Nadat alle lagen zijn samengevoegd, wordt de samengestelde afbeelding omgezet in de uiteindelijke reactieafbeelding, zoals opgegeven met de opdracht [opdrachten en kenmerken weergeven](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90).
