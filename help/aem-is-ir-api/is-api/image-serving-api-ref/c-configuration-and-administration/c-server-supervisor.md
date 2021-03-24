---
description: Beeld dat componenten serveert wordt beheerd door de Supervisor van de Server, die een Linux daemon of Dienst van Vensters (S7Supervisor.exe is, die als "Beeld van Dynamic Media Servend"in het Controlebord van de Diensten wordt vermeld).
solution: Experience Manager
title: Servertoezichthouder
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder,praktijkgericht
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---


# Servertoezichthouder{#server-supervisor}

Beeld dat componenten serveert wordt beheerd door de Supervisor van de Server, die een Linux daemon of Dienst van Vensters (S7Supervisor.exe is, die als &quot;Beeld van Dynamic Media Servend&quot;in het Controlebord van de Diensten wordt vermeld).

Naast het beginnen en het tegenhouden van andere Beeld die componenten dienen, is de Supervisor van de Server verantwoordelijk voor het verzekeren van de gezondheid van deze andere componenten. Als een component vastloopt, wordt het automatisch opnieuw begonnen om om het even welke de dienstonderbrekingen te minimaliseren.

## {#section-061d28d74e034a30adc39ea3e2031cd0} starten en stoppen

De Supervisor van de Server is begonnen, tegengehouden, en opnieuw begonnen met het Beeld dat hulpprogrammascript van het nut dienen. Raadpleeg de [documentatie bij Hulpprogramma&#39;s](../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f) voor meer informatie.

Het beginnen en het tegenhouden van de Supervisor van de Server begint automatisch en houdt alle andere Beeld dat componenten dienen tegen.

[SupervisorRegistry.xml](../../../is-api/image-serving-api-ref/c-configuration-and-administration/r-server-configuration-files/r-supervisorregistry.md#reference-b55f37a7a7a044d19c1722f5130906c6)
