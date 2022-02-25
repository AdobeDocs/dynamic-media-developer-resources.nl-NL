---
title: Technische ondersteuning
description: Alle viewercomponenten ondersteunen de rollen en kenmerken van ARIA (Accessible Rich Internet Applications) om de integratie met ondersteunende hulpmiddelen, zoals schermlezers, te verbeteren.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom,Accessibility
role: Developer,User
exl-id: f2f36520-f6dd-4baa-abf0-48a846882acb
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# Technische ondersteuning{#assistive-technology-support}

Alle viewercomponenten ondersteunen de rollen en kenmerken van ARIA (Accessible Rich Internet Applications) om de integratie met ondersteunende hulpmiddelen, zoals schermlezers, te verbeteren.

Het viewerelement op het hoogste niveau heeft een rol `region` en `aria-label` kenmerk standaard ingesteld op de naam van de viewer. U kunt het label besturen met het `Container.LABEL` lokalisatiesymbool.

Knoppen hebben de rol `button` en beschrijvende tekst ingesteld met de `aria-label` kenmerk. De waarde van `aria-label` wordt gevuld met de waarde van het localisatiesymbool van de knop. Wanneer een knop is uitgeschakeld, wordt `aria-disabled` wordt dienovereenkomstig ingesteld.

De hoofdweergave heeft een rol `application`. Een korte beschrijving van het hoofdstandpunt wordt gegeven in `aria-roledescription`met de waarde die door de `ROLE_DESCRIPTION` lokalisatiesymbool van de bijbehorende hoofdweergavecomponent. Navigatietips voor toetsenbordgebruikers worden weergegeven met `aria-describedby`, de tekst voor de gebruikstip afkomstig is van de `USAGE_HINT` lokalisatiesymbool. Als voor een element een label is gedefinieerd in het veld UserData, wordt `aria-label` wordt ingesteld met de waarde van een dergelijk label.
