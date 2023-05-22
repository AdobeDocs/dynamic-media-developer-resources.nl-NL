---
description: Met de viewer kunt u de inhoud van de catalogus uitvoeren naar een printer.
solution: Experience Manager
title: Afdrukken, functie
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: eadcc105-4a86-40f7-867a-3b09a5599a41
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 0%

---

# Afdrukken, functie{#print-feature}

Met de viewer kunt u de inhoud van de catalogus uitvoeren naar een printer.

De afdrukfunctie wordt geactiveerd door een specifieke knop op de werkbalk. Als u op de knop klikt, kan de gebruiker een afdrukbereik en het aantal pagina&#39;s per vel kiezen.

De kwaliteit van de afdruk kan worden aangepast met de `printquality` configuratieparameter. Merk op dat het plaatsen `printquality` aan waarden beduidend hoger dan het gebrek wordt niet geadviseerd. De reden hiervoor is dat dit leidt tot een zeer hoog geheugengebruik door de webbrowser op het clientsysteem. Zorg er ook voor dat de maximale responsgrootte voor het image die voor uw Dynamic Media Classic-bedrijf is ingesteld, groter is dan de geconfigureerde `printquality` waarde.

>[!NOTE]
>
>De functie Afdrukken is alleen beschikbaar op desktopsystemen, behalve Internet Explorer 9.
