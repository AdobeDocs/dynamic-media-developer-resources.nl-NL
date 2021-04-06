---
description: Alle viewercomponenten ondersteunen de rollen en kenmerken van ARIA (Accessible Rich Internet Applications) om de integratie met ondersteunende hulpmiddelen, zoals schermlezers, te verbeteren.
solution: Experience Manager
title: Technische ondersteuning
feature: Dynamic Media Classic,Viewers,SDK/API,Interactieve afbeeldingen,Toegankelijkheid
role: Ontwikkelaar,zakelijke praktiserer
exl-id: 39e64f35-543f-4977-a97a-0daa93786ff3
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 0%

---

# Support voor ondersteunende hulpmiddelen{#assistive-technology-support}

Alle viewercomponenten ondersteunen de rollen en kenmerken van ARIA (Accessible Rich Internet Applications) om de integratie met ondersteunende hulpmiddelen, zoals schermlezers, te verbeteren.

Het viewerelement op het hoogste niveau heeft het kenmerk rol `region` en `aria-label` standaard ingesteld op de naam van de viewer. U kunt het label besturen met het lokalisatiesymbool `Container.LABEL`.

De hoofdweergave heeft de rol `application`. Een korte beschrijving van de hoofdweergave vindt u in `aria-roledescription`, met de waarde die wordt gedefinieerd door het lokalisatiesymbool `ROLE_DESCRIPTION` van de overeenkomstige hoofdweergavecomponent. Navigatietips voor toetsenbordgebruikers worden opgegeven met `aria-describedby`. De tekst voor de gebruikshint is afkomstig van het `USAGE_HINT`-lokalisatiesymbool. Als voor een element een label is gedefinieerd in het veld UserData, wordt het kenmerk `aria-label` ingesteld met de waarde van een dergelijk label.

Hot spots, gebieden en afbeeldingen met hyperlinks hebben de rol `button` en beschrijvende tekst ingesteld met het kenmerk `aria-label`, met de waarde van de hotspot of het label van de afbeeldingskaart. Wanneer de gebruiker focus op hotspots of afbeeldingen met hyperlinks plaatst, worden navigatietekens voor toetsenbordgebruikers opgegeven met `aria-describedby`, waarbij de tekst voor de gebruikshint afkomstig is van het `USAGE_HINT`-lokalisatiesymbool.
