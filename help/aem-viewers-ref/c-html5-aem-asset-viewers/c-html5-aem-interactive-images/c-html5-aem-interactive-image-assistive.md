---
description: Alle viewercomponenten ondersteunen de rollen en kenmerken van ARIA (Accessible Rich Internet Applications) om de integratie met ondersteunende hulpmiddelen, zoals schermlezers, te verbeteren.
solution: Experience Manager
title: Technische ondersteuning
feature: Dynamic Media Classic,Viewers,SDK/API,Interactieve afbeeldingen,Toegankelijkheid
role: Developer,User
exl-id: 39e64f35-543f-4977-a97a-0daa93786ff3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# Technische ondersteuning{#assistive-technology-support}

Alle viewercomponenten ondersteunen de rollen en kenmerken van ARIA (Accessible Rich Internet Applications) om de integratie met ondersteunende hulpmiddelen, zoals schermlezers, te verbeteren.

Het viewerelement op het hoogste niveau heeft het kenmerk rol `region` en `aria-label` standaard ingesteld op de naam van de viewer. U kunt het label besturen met het lokalisatiesymbool `Container.LABEL`.

De hoofdweergave heeft de rol `application`. Een korte beschrijving van de hoofdweergave vindt u in `aria-roledescription`, met de waarde die wordt gedefinieerd door het lokalisatiesymbool `ROLE_DESCRIPTION` van de overeenkomstige hoofdweergavecomponent. Navigatietips voor toetsenbordgebruikers worden opgegeven met `aria-describedby`. De tekst voor de gebruikshint is afkomstig van het `USAGE_HINT`-lokalisatiesymbool. Als voor een element een label is gedefinieerd in het veld UserData, wordt het kenmerk `aria-label` ingesteld met de waarde van een dergelijk label.

Hot spots, gebieden en afbeeldingen met hyperlinks hebben de rol `button` en beschrijvende tekst ingesteld met het kenmerk `aria-label`, met de waarde van de hotspot of het label van de afbeeldingskaart. Wanneer de gebruiker focus op hotspots of afbeeldingen met hyperlinks plaatst, worden navigatietekens voor toetsenbordgebruikers opgegeven met `aria-describedby`, waarbij de tekst voor de gebruikshint afkomstig is van het `USAGE_HINT`-lokalisatiesymbool.
