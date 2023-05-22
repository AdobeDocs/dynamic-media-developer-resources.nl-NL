---
title: Technische ondersteuning
description: Alle viewercomponenten ondersteunen de rollen en kenmerken van ARIA (Accessible Rich Internet Applications) om de integratie met ondersteunende hulpmiddelen, zoals schermlezers, te verbeteren.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners,Accessibility
role: Developer,User
exl-id: 3ed943e8-4695-4561-9be0-1b6ed30294f8
source-git-commit: 4aaa77b1fb58b30b02ee15f6080169fa354d5907
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---

# Technische ondersteuning{#assistive-technology-support}

Alle viewercomponenten ondersteunen de rollen en kenmerken van ARIA (Accessible Rich Internet Applications) om de integratie met ondersteunende hulpmiddelen, zoals schermlezers, te verbeteren.

Het viewerelement op het hoogste niveau heeft een rol `region` en `aria-label` kenmerk standaard ingesteld op de naam van de viewer. U kunt het label besturen met het `Container.LABEL` lokalisatiesymbool.

Knoppen hebben de rol `button` en beschrijvende tekst ingesteld met `aria-label` kenmerk. De waarde van `aria-label` wordt gevuld met de waarde van het localisatiesymbool van de knop. Wanneer een knop is uitgeschakeld, `aria-disabled` wordt dienovereenkomstig ingesteld.

Knoppen waarmee u door carrouseldia&#39;s kunt navigeren, bevatten labels die tijdens de uitvoering worden bijgewerkt, afhankelijk van de geselecteerde dia. De sjabloon voor deze knoppenlabel wordt ingesteld met `CAROUSELVIEWER_TOOLTIP_GOTO` lokalisatiesymbool.

De hoofdweergave heeft een rol `application`. Een korte beschrijving van het hoofdstandpunt wordt gegeven in `aria-roledescription`met de waarde die door de `ROLE_DESCRIPTION` lokalisatiesymbool van de bijbehorende hoofdweergavecomponent. Navigatietips voor toetsenbordgebruikers worden weergegeven met `aria-describedby`, de tekst voor de gebruikstip afkomstig is van de `USAGE_HINT` lokalisatiesymbool. Als voor een element een label is gedefinieerd in het veld UserData, wordt `aria-label` wordt ingesteld met de waarde van een dergelijk label.

Hotspots, gebieden en afbeeldingen met hyperlinks hebben de rol `button` en beschrijvende tekst ingesteld met `aria-label` met de waarde van de hotspot of het label van de afbeelding met hyperlinks. Wanneer de gebruiker de focus op hotspots of afbeeldingen met hyperlinks plaatst, worden navigatietekens voor toetsenbordgebruikers weergegeven met `aria-describedby`, met de tekst voor de gebruiksaanwijzing die afkomstig is van de `USAGE_HINT` lokalisatiesymbool.
