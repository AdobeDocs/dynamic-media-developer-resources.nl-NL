---
description: Gebruik deze serverinstellingen om het bewakings- en waarschuwingssysteem te configureren.
solution: Experience Manager
title: Toezicht- en waarschuwingssysteem
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: fe672d1b-93e5-466a-a329-3032095c6ba8
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---

# Toezicht- en waarschuwingssysteem{#monitoring-and-alerting-system}

Gebruik deze serverinstellingen om het bewakings- en waarschuwingssysteem te configureren.

## AS::monitorAlertGenerator.enableGlobalAlerting - Waarschuwingssysteem inschakelen {#section-612f8ea61794426ab205e22e5f665fa9}

Schakel e-mailmeldingen in door de instelling &#39;true&#39; in te stellen en de instellingen voor e-mailmeldingen te configureren. Instellen op `false` Hiermee schakelt u alle e-mailwaarschuwingen uit. Dit kan handig zijn wanneer u een server offline zet voor onderhoud. Booleaans.

## AS::mailSender.host - SMTP-host {#section-151df07e7b44446581339bb7abeeba7a}

Het IP-adres van de SMTP-e-mailserver.

## AS::mailSender.port- SMTP-poort {#section-4b25efca8fd84d5c92dafacd0555e99d}

De luisterpoort voor de SMTP-e-mailserver.

## AS::monitorAlertGenerator.messageTo - Message Recipient {#section-0017bbaa15434117a70900c3f1163960}

Een of meer e-mailadressen waarnaar waarschuwingen moeten worden verzonden. Gebruik puntkomma&#39;s als scheidingstekens.

## AS:monitorAlertGenerator.messageFrom - Message Sender {#section-db320cba4ac2438ca1cfe6abce4aed87}

Het e-mailadres dat moet worden gebruikt in het dialoogvenster **[!UICONTROL From]** e-mailveld.

## AS::monitorAlertGenerator.alertInterval - Monitoring Interval {#section-99cb2e3380c1499e9d5aec3671ed73c7}

Het bewakingssysteem accumuleert alarmcondities tijdens het waarschuwingsinterval en stuurt een waarschuwings-e-mail met alle geaccumuleerde waarschuwingen aan het einde van elk interval. Milliseconden, geheel getal, 60000 of groter. Wordt meestal ingesteld op 5 of 10 minuten.

## AS::monitorAlertGenerator.heapSpaceResetInterval - Waarschuwingsinterval voor heapruimte {#section-fd5a2bf04ed44fdcaef20f77084151a8}

Minimumtijd na een heapspatie-waarschuwing voordat een andere wordt uitgegeven. Intervaltijd in msec. Geheel getal, 0 of groter.

## AS::monitorAlertGenerator.minTrafficForAlerts - MinimumVerkeer om het Alarm toe te laten {#section-8b4db2d6f96642309ca35c49eb3ab230}

Verzoeken per seconde. Er worden geen responstijd en foutmeldingen verzonden als het verkeer onder deze drempel valt. Reeks aan 0 om reactietijd en foutenalarm ongeacht het verkeersvolume te verzenden. Reële waarde 0 of hoger.
