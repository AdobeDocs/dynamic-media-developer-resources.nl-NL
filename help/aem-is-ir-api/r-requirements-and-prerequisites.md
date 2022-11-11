---
description: Controleer voordat u Dynamic Media Image Serving gebruikt of uw systeem voldoet aan de systeemvereisten.
solution: Experience Manager
title: Systeemvereisten en -vereisten
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea2dfec9-0a42-4ccb-8442-6f7c4a39eda1
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---

# Systeemvereisten en -vereisten{#system-requirements-and-prerequisites}

Controleer voordat u Dynamic Media Image Serving gebruikt of uw systeem voldoet aan de systeemvereisten.

## Serverhardware {#section-f3c14a7bc1b745118602659628df779f}

Uw server moet voldoen aan de volgende hardwarevereisten.

>[!NOTE]
>
>Systemen met processors met AMD64 en Intel® EM64T worden doorgaans geconfigureerd als NUMA (Non-Uniform Memory Architecture)-platforms. Dit betekent dat de kernel veelvoudige geheugenknopen bij laars-tijd eerder dan het construeren van één enkele geheugenknoop bouwt. De meervoudige knoopaannemer kan in geheugenuitputting op één of meerdere knopen resulteren alvorens andere knopen worden uitgeput. Wanneer de geheugenuitputting gebeurt kan de pit besluiten om processen (bijvoorbeeld de Server van het Beeld of [!DNL Platform Server]), ook al is er geheugen beschikbaar. Daarom adviseert Adobe Systems dat als u zulk een systeem in werking stelt u NUMA uitzet. Gebruik de `numa=off` start optie om te voorkomen dat de kernel deze processen tegenhoudt.

**Windows**

* Intel Xeon® of AMD® Opteron CPU met ten minste vier kernen.
* Minimaal 16 GB RAM.
* Ruimte wisselen gelijk aan minstens tweemaal de hoeveelheid fysiek geheugen (RAM).
* 2 GB beschikbare ruimte op de vaste schijf voor de installatie en de basisbewerking; er is meer schijfruimte vereist voor bronafbeeldingen, logbestanden, gegevenscache en manifestbestanden.
* Snelle Ethernet-netwerkinterfacekaart.

**Linux**

* Intel Xeon® of AMD® Opteron CPU met ten minste vier kernen.
* Minimaal 16 GB RAM.
* Wisselen uitgeschakeld (aanbevolen).
* 2 GB beschikbare ruimte op de vaste schijf voor de installatie en de basisbewerking; er is meer schijfruimte vereist voor bronafbeeldingen, logbestanden, gegevenscache en manifestbestanden.
* Snelle Ethernet-netwerkinterfacekaart.

**Opmerking (Linux):** De service Image Serving werkt niet wanneer SELinux is ingeschakeld. Deze optie is standaard ingeschakeld. Als u SELinux wilt uitschakelen, bewerkt u de [!DNL /etc/selinux/config] en wijzig de SELinux-waarde van:

`SELINUX=enforcing`

tot

`SELINUX=disabled`

**Opmerking (Linux):** Zorg ervoor dat de gastheernaam van de server aan een IP adres oplosbaar is. Als dat niet mogelijk is, voeg volledig - gekwalificeerde gastheernaam en het IP adres aan toe [!DNL /etc/hosts] zoals in het volgende voorbeeld.

`<ip address> <fully qualified hostname>`

## Serversoftware {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

Voor Dynamic Media Image Serving is de volgende serversoftware vereist.

**Windows**

* Microsoft® Windows 2008 Server.
* 64-bits besturingssysteem.

**Linux**

* Red Hat® Enterprise 5 of CentOS 5.5 en hoger, met de nieuwste herstelpatches.
* 64-bits besturingssysteem.

**Opmerking:** Om Beeld te gebruiken die op Vensters dienen, moet u Microsoft Visual Studio 2010 redistributable installeren.
