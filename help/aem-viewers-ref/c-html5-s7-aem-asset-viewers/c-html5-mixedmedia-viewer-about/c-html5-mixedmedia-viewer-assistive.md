---
description: Alle viewercomponenten ondersteunen de rollen en kenmerken van ARIA (Accessible Rich Internet Applications) om de integratie met ondersteunende hulpmiddelen, zoals schermlezers, te verbeteren.
seo-description: Alle viewercomponenten ondersteunen de rollen en kenmerken van ARIA (Accessible Rich Internet Applications) om de integratie met ondersteunende hulpmiddelen, zoals schermlezers, te verbeteren.
seo-title: Technische ondersteuning
solution: Experience Manager
title: Technische ondersteuning
topic: Dynamic media
uuid: 4a84a3a6-e9ba-4511-8228-e1a611f871c0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Technische ondersteuning{#assistive-technology-support}

Alle viewercomponenten ondersteunen de rollen en kenmerken van ARIA (Accessible Rich Internet Applications) om de integratie met ondersteunende hulpmiddelen, zoals schermlezers, te verbeteren.

Voor het viewerelement op het hoogste niveau zijn de rol `region` en het `aria-label` kenmerk standaard ingesteld op de naam van de viewer. U kunt het label besturen met het `Container.LABEL` lokalisatiesymbool.

Knoppen hebben de rol `button` en beschrijvende tekst ingesteld met `aria-label` kenmerk. De waarde van het `aria-label` kenmerk wordt gevuld met de waarde van het localisatiesymbool van de knop. Wanneer een knop is uitgeschakeld, wordt het `aria-disabled` kenmerk dienovereenkomstig ingesteld.

De hoofdrol is weggelegd `application`. U vindt een korte beschrijving van de hoofdweergave in `aria-roledescription`, waarbij de waarde wordt gedefinieerd door het `ROLE_DESCRIPTION` lokalisatiesymbool van de overeenkomstige hoofdweergavecomponent. Navigatietips voor toetsenbordgebruikers worden gebruikt. `aria-describedby`De tekst voor de gebruiksaanwijzing is afkomstig van het `USAGE_HINT` lokalisatiesymbool. Als voor een element een label is gedefinieerd in het veld UserData, wordt het `aria-label` kenmerk ingesteld met de waarde van dat label.

Componenten die stalen weergeven, hebben de rol `listbox` met `aria-label` kenmerk ingesteld op de waarde van het `LABEL` lokalisatiesymbool van die component. Afzonderlijke stalen hebben de rol `option` met `aria-setsize` en `aria-posinset` kenmerken om de staalpositie in de set te beschrijven. Als een staal is geselecteerd, wordt het `aria-selected` kenmerk ingesteld op `true`.

De componenten van de schuif hebben de rol `slider` met attributen `aria-valuenow`, `aria-valuemin`en `aria-valuemax` om de huidige schuifbalkpositie te beschrijven.
