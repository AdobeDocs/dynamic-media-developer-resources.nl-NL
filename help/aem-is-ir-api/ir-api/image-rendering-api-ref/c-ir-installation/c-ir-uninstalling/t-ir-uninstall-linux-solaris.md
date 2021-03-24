---
description: Volg deze instructies om het renderen van afbeeldingen op een Linux- of Solaris-systeem te verwijderen.
solution: Experience Manager
title: Verwijderen op Linux en Solaris
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---


# Verwijderen op Linux en Solaris{#uninstalling-on-linux-and-solaris}

Volg deze instructies om het renderen van afbeeldingen op een Linux- of Solaris-systeem te verwijderen.

Er zijn twee manieren om het Teruggeven van het Beeld op een systeem van Linux of Solaris te desinstalleren.

**Methode 1**

1. Zoeken [!DNL uninstall.sh].

   Het bevindt zich in de map waaruit ImageRendering is geïnstalleerd. Als deze map is verwijderd, moet het originele installatiepakket niet zijn gecomprimeerd en niet zijn doorgevoerd om [!DNL uninstall.sh] te kunnen extraheren.
1. Voer [!DNL uninstall.sh] uit en volg de instructies op het scherm.

>**Methode 2**
>
>1. ImageRendering stoppen met: ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`
>1. Verwijder ImageRendering van uw systeem.

>
>   
De opdracht om ImageRendering te verwijderen is afhankelijk van uw systeem:
>
>   Linux: `rpm -e ImageRendering`
>
>   Solaris: `pkgrm ImageRendering`
>
>1. Verwijder directory&#39;s of bestanden die niet zijn verwijderd in Stap 2.

>



