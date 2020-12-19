---
description: Controleer voordat u Scene7 Image Serving gebruikt of uw systeem voldoet aan de systeemvereisten.
seo-description: Controleer voordat u Scene7 Image Serving gebruikt of uw systeem voldoet aan de systeemvereisten.
seo-title: Systeemvereisten en -vereisten
solution: Experience Manager
title: Systeemvereisten en -vereisten
topic: Scene7 Image Serving - Image Rendering API
uuid: 80196574-f5a2-4298-880a-cc36f90b6e21
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 0%

---


# Systeemvereisten en -vereisten{#system-requirements-and-prerequisites}

Controleer voordat u Scene7 Image Serving gebruikt of uw systeem voldoet aan de systeemvereisten.

## Serverhardware {#section-f3c14a7bc1b745118602659628df779f}

Uw server moet voldoen aan de volgende hardwarevereisten.

>[!NOTE]
>
>Systemen met processors met AMD64 en Intel® EM64T worden doorgaans geconfigureerd als NUMA (Non-Uniform Memory Architecture)-platforms. Dit betekent dat de kernel veelvoudige geheugenknopen bij laars-tijd eerder dan het construeren van één enkele geheugenknoop bouwt. De meervoudige knoopaannemer kan in geheugenuitputting op één of meerdere knopen resulteren alvorens andere knopen worden uitgeput. Wanneer de geheugenuitputting gebeurt kan de pit besluiten om processen (bijvoorbeeld, de Server van het Beeld of de Server van het Platform) te doden alhoewel er beschikbaar geheugen is. Daarom adviseert Adobe Systems dat als u zulk een systeem in werking stelt u NUMA uitzet. Gebruik de startoptie `numa=off` om te voorkomen dat de kernel deze processen tegenhoudt.

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

**Opmerking (Linux):** Afbeeldingsservice werkt niet wanneer SELinux is ingeschakeld. Deze optie is standaard ingeschakeld. Om SELinux onbruikbaar te maken, geef het [!DNL /etc/selinux/config] dossier uit en verander de waarde SELinux van:

`SELINUX=enforcing`

tot

`SELINUX=disabled`

**Opmerking (Linux):** zorg ervoor dat de hostnaam van de server kan worden omgezet naar een IP-adres. Als dat niet mogelijk is, voeg volledig - gekwalificeerde gastheernaam en het IP adres aan [!DNL /etc/hosts] zoals in het volgende voorbeeld toe.

`<ip address> <fully qualified hostname>`

## Serversoftware {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

Voor Scene7 Image Serving is de volgende serversoftware vereist.

**Windows**

* Microsoft® Windows 2008 Server.
* 64-bits besturingssysteem.

**Linux**

* Red Hat® Enterprise 5 of CentOS 5.5 en hoger, met de nieuwste herstelpatches.
* 64-bits besturingssysteem.

**Nota:** om Beeld te gebruiken die op Vensters dienen, moet u Microsoft Visual Studio 2010 redistributable installeren. Redistributable is beschikbaar op de volgende plaats:

[http://www.microsoft.com/en-us/download/details.aspx?id=13523](http://www.microsoft.com/en-us/download/details.aspx?id=13523)

