---
description: Alvorens het Beeld te gebruiken Scene7 Serving, zorg ervoor uw systeem aan de systeemvereisten voldoet.
seo-description: Alvorens het Beeld te gebruiken Scene7 Serving, zorg ervoor uw systeem aan de systeemvereisten voldoet.
seo-title: Systeemvereisten en -vereisten
solution: Experience Manager
title: Systeemvereisten en -vereisten
topic: Scene7 Image Serving - Image Rendering API
uuid: 80196574-f5a2-4298-880a-cc36f90b6e21
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Systeemvereisten en -vereisten{#system-requirements-and-prerequisites}

Alvorens het Beeld te gebruiken Scene7 Serving, zorg ervoor uw systeem aan de systeemvereisten voldoet.

## Serverhardware {#section-f3c14a7bc1b745118602659628df779f}

Uw server moet voldoen aan de volgende hardwarevereisten.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>Systemen met processors met AMD64 en Intel® EM64T worden doorgaans geconfigureerd als NUMA (Non-Uniform Memory Architecture)-platforms. Dit betekent dat de kernel veelvoudige geheugenknopen bij laars-tijd eerder dan het construeren van één enkele geheugenknoop bouwt. De meervoudige knoopaannemer kan in geheugenuitputting op één of meerdere knopen resulteren alvorens andere knopen worden uitgeput. Wanneer de geheugenuitputting gebeurt kan de pit besluiten om processen (bijvoorbeeld, de Server van het Beeld of de Server van het Platform) te doden alhoewel er beschikbaar geheugen is. Daarom raadt Adobe Systems u aan NUMA uit te schakelen als u een dergelijk systeem uitvoert. Gebruik de `numa=off` startoptie om te voorkomen dat de kernel deze processen tegenhoudt.

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

**Opmerking (Linux):** De service Image Serving werkt niet wanneer SELinux is ingeschakeld. Deze optie is standaard ingeschakeld. Als u SELinux wilt uitschakelen, bewerkt u het [!DNL /etc/selinux/config] bestand en wijzigt u de SELinux-waarde van:

`SELINUX=enforcing`

tot

`SELINUX=disabled`

**Opmerking (Linux):** Zorg ervoor dat de gastheernaam van de server aan een IP adres oplosbaar is. Als dat niet mogelijk is, voeg volledig - gekwalificeerde gastheernaam en het IP adres aan [!DNL /etc/hosts] zoals in het volgende voorbeeld toe.

`<ip address> <fully qualified hostname>`

## Serversoftware {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

Voor Scene7 Image Serving is de volgende serversoftware vereist.

**Windows**

* Microsoft® Windows 2008 Server.
* 64-bits besturingssysteem.

**Linux**

* Red Hat® Enterprise 5 of CentOS 5.5 en hoger, met de nieuwste herstelpatches.
* 64-bits besturingssysteem.

**Opmerking:** Om Beeld te gebruiken die op Vensters dienen, moet u Microsoft Visual Studio 2010 redistributable installeren. Redistributable is beschikbaar op de volgende plaats:

[http://www.microsoft.com/en-us/download/details.aspx?id=13523](http://www.microsoft.com/en-us/download/details.aspx?id=13523)

