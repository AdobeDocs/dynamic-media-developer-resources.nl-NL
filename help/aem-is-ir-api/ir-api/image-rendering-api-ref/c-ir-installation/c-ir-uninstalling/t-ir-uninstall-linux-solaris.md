---
title: Verwijderen op Linux® en Solaris™
description: Volg deze instructies om het renderen van afbeeldingen op een Linux®- of Solaris™-systeem te verwijderen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c81feaba-18da-441a-bfd5-40275558a384
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---

# Verwijderen op Linux® en Solaris™{#uninstalling-on-linux-and-solaris}

Volg deze instructies om het renderen van afbeeldingen op een Linux®- of Solaris™-systeem te verwijderen. U kunt twee verschillende methoden gebruiken. Voer een van de volgende handelingen uit:

## Methode 1

1. Zoeken [!DNL uninstall.sh].

   Het bevindt zich in de map van waaruit ImageRendering is geïnstalleerd. Als deze map is verwijderd, moet het originele installatiepakket niet zijn gecomprimeerd en niet zijn doorgevoerd om te kunnen worden uitgepakt [!DNL uninstall.sh].
1. Uitvoeren [!DNL uninstall.sh] en volgt u de aanwijzingen op het scherm.

## Methode 2

1. Stop ImageRendering met het volgende:

   ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`

1. Verwijder ImageRendering van uw systeem. De opdracht die u gebruikt, is afhankelijk van uw systeem.
   * Linux®: `rpm -e ImageRendering`

   * Solaris™: `pkgrm ImageRendering`

1. Verwijder directory&#39;s of bestanden die niet zijn verwijderd in stap 2.

