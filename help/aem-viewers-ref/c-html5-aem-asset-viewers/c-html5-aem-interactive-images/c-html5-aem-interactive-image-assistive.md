---
title: Technische ondersteuning
description: Alle viewercomponenten ondersteunen de rollen en kenmerken van ARIA (Accessible Rich Internet Applications) om de integratie met ondersteunende hulpmiddelen, zoals schermlezers, te verbeteren.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images,Accessibility
role: Developer,User
exl-id: 39e64f35-543f-4977-a97a-0daa93786ff3
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# Technische ondersteuning{#assistive-technology-support}

Alle viewercomponenten ondersteunen de rollen en kenmerken van ARIA (Accessible Rich Internet Applications) om de integratie met ondersteunende hulpmiddelen, zoals schermlezers, te verbeteren.

Het viewerelement op het hoogste niveau heeft een rol `region` en `aria-label` kenmerk standaard ingesteld op de naam van de viewer. U kunt het label besturen met het `Container.LABEL` lokalisatiesymbool.

De hoofdweergave heeft een rol `application`. Een korte beschrijving van het hoofdstandpunt wordt gegeven in `aria-roledescription`met de waarde die door de `ROLE_DESCRIPTION` lokalisatiesymbool van de bijbehorende hoofdweergavecomponent. Navigatietips voor toetsenbordgebruikers worden weergegeven met `aria-describedby`, de tekst voor de gebruikstip afkomstig is van de `USAGE_HINT` lokalisatiesymbool. Als voor een element een label is gedefinieerd in het veld UserData, wordt `aria-label` wordt ingesteld met de waarde van een dergelijk label.

Hotspots, gebieden en afbeeldingen met hyperlinks hebben de rol `button` en beschrijvende tekst ingesteld met `aria-label` met de waarde van de hotspot of het label van de afbeelding met hyperlinks. Wanneer de gebruiker de focus op hotspots of afbeeldingen met hyperlinks plaatst, worden navigatietekens voor toetsenbordgebruikers weergegeven met `aria-describedby`, met de tekst voor de gebruiksaanwijzing die afkomstig is van de `USAGE_HINT` lokalisatiesymbool.
