---
description: Alle viewercomponenten ondersteunen de rollen en kenmerken van ARIA (Accessible Rich Internet Applications) om de integratie met ondersteunende hulpmiddelen, zoals schermlezers, te verbeteren.
seo-description: Alle viewercomponenten ondersteunen de rollen en kenmerken van ARIA (Accessible Rich Internet Applications) om de integratie met ondersteunende hulpmiddelen, zoals schermlezers, te verbeteren.
seo-title: Technische ondersteuning
solution: Experience Manager
title: Technische ondersteuning
topic: Dynamic media
uuid: 6312f2f7-e1fa-4536-bae4-d8bc7735d5af
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---


# Support voor ondersteunende hulpmiddelen{#assistive-technology-support}

Alle viewercomponenten ondersteunen de rollen en kenmerken van ARIA (Accessible Rich Internet Applications) om de integratie met ondersteunende hulpmiddelen, zoals schermlezers, te verbeteren.

Het viewerelement op het hoogste niveau heeft het kenmerk rol `region` en `aria-label` standaard ingesteld op de naam van de viewer. U kunt het label besturen met het lokalisatiesymbool `Container.LABEL`.

Knoppen hebben de rol `button` en beschrijvende tekst ingesteld met `aria-label` kenmerk. De waarde van het kenmerk `aria-label` wordt gevuld met de waarde van het localisatiesymbool van de knop. Wanneer een knoop gehandicapt is, `aria-disabled` wordt attributen geplaatst dienovereenkomstig.

De hoofdweergave heeft de rol `application`. Een korte beschrijving van de hoofdweergave vindt u in `aria-roledescription`, met de waarde die wordt gedefinieerd door het lokalisatiesymbool `ROLE_DESCRIPTION` van de overeenkomstige hoofdweergavecomponent. Navigatietips voor toetsenbordgebruikers worden opgegeven met `aria-describedby`. De tekst voor de gebruikshint is afkomstig van het `USAGE_HINT`-lokalisatiesymbool. Als voor een element een label is gedefinieerd in het veld UserData, wordt het kenmerk `aria-label` ingesteld met de waarde van een dergelijk label.
