---
description: Alle viewercomponenten ondersteunen de rollen en kenmerken van ARIA (Accessible Rich Internet Applications) om de integratie met ondersteunende hulpmiddelen, zoals schermlezers, te verbeteren.
seo-description: Alle viewercomponenten ondersteunen de rollen en kenmerken van ARIA (Accessible Rich Internet Applications) om de integratie met ondersteunende hulpmiddelen, zoals schermlezers, te verbeteren.
seo-title: Technische ondersteuning
solution: Experience Manager
title: Technische ondersteuning
topic: Dynamic media
uuid: 72b414f4-b647-4afa-a409-a8ba90227d3f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Technische ondersteuning{#assistive-technology-support}

Alle viewercomponenten ondersteunen de rollen en kenmerken van ARIA (Accessible Rich Internet Applications) om de integratie met ondersteunende hulpmiddelen, zoals schermlezers, te verbeteren.

Voor het viewerelement op het hoogste niveau zijn de rol `region` en het `aria-label` kenmerk standaard ingesteld op de naam van de viewer. U kunt het label besturen met het `Container.LABEL` lokalisatiesymbool.

Knoppen hebben de rol `button` en beschrijvende tekst ingesteld met `aria-label` kenmerk. De waarde van het `aria-label` kenmerk wordt gevuld met de waarde van het localisatiesymbool van de knop. Wanneer een knop is uitgeschakeld, wordt het `aria-disabled` kenmerk dienovereenkomstig ingesteld.

Knoppen waarmee u door carrouseldia&#39;s kunt navigeren, bevatten labels die tijdens de uitvoering worden bijgewerkt, afhankelijk van de geselecteerde dia. De sjabloon voor het label van deze knop wordt ingesteld met een `CAROUSELVIEWER_TOOLTIP_GOTO` lokalisatiesymbool.

De hoofdrol is weggelegd `application`. U vindt een korte beschrijving van de hoofdweergave in `aria-roledescription`, waarbij de waarde wordt gedefinieerd door het `ROLE_DESCRIPTION` lokalisatiesymbool van de overeenkomstige hoofdweergavecomponent. Navigatietips voor toetsenbordgebruikers worden gebruikt. `aria-describedby`De tekst voor de gebruiksaanwijzing is afkomstig van het `USAGE_HINT` lokalisatiesymbool. Als voor een element een label is gedefinieerd in het veld UserData, wordt het `aria-label` kenmerk ingesteld met de waarde van dat label.

Hotspots, gebieden en afbeeldingen met hyperlinks hebben de rol `button` en beschrijvende tekst ingesteld met `aria-label` kenmerk, met de waarde van het label voor hotspot of afbeeldingskaart. Wanneer de gebruiker de focus op hotspots of afbeeldingen met hyperlinks plaatst, worden er navigatietekens voor toetsenbordgebruikers weergegeven, `aria-describedby`waarbij de tekst voor de gebruiksaanwijzing afkomstig is van het `USAGE_HINT` lokalisatiesymbool.
