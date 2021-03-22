---
description: Deze sectie bevat oplossingen voor problemen die af en toe met het Serven van het Beeld zijn voorgekomen.
seo-description: Deze sectie bevat oplossingen voor problemen die af en toe met het Serven van het Beeld zijn voorgekomen.
seo-title: Problemen oplossen
solution: Experience Manager
title: Problemen oplossen
uuid: 39fdaf86-004b-4553-bde0-0367f3ef76b8
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 0%

---


# Problemen oplossen{#troubleshooting}

Deze sectie bevat oplossingen voor problemen die af en toe met het Serven van het Beeld zijn voorgekomen.

**Algemeen**

ImageServer houdt nu een installatielogboekbestand bij en een back-upmap met alle bestanden die tijdens een upgrade-installatie zijn gewijzigd. Dit bestand en deze map bevinden zich in de hoofdmap van de installatiemap van de ImageServing.

**Wanneer het beginnen van de Server van het Beeld, stapelt het startmanuscript met het bericht &quot;begin in afwachting&quot; (LINUX slechts)**

Dit kan wijzen op een probleem met de Beeldserver- Vergunning, zoals een ontbrekend vergunningsdossier of een verlopen tijdelijke vergunning. Een geldig licentiebestand moet zich in [!DNL /usr/local/scene7/licenses] bevinden.

**Afbeeldingsserver loopt vast of loopt vast en het logbestand van de afbeeldingsserver geeft aan dat er onvoldoende ruimte is of dat de bron tijdelijk niet beschikbaar is in het bestand  [!DNL IgcVirtualMemory.cpp]&quot;**

De reden voor dit foutenbericht is dat de Server van het Beeld er niet in is geslaagd om de hoeveelheid geheugen toe te wijzen het aan gebruik werd gevormd.

* Controleer de instelling Fysiek geheugen in [!DNL ImageServerRegistry.xml]. Het zou niet meer dan 50%, minder moeten zijn als andere geheugen-intensieve toepassingen op het zelfde systeem lopen. De standaardwaarde is 20%.
* Zorg ervoor dat de ruilruimte op de Server minstens tweemaal de grootte van fysiek RAM is. Dit probleem kan worden veroorzaakt door instellingen voor weinig wisselruimte.

**De werkelijke schijfruimte die door de cachemap wordt gebruikt, overschrijdt de  ` *[!DNL cache.maxSize]*`set in[!DNL PlatformServer.conf]**

Dit duidt niet op een probleem. De overhead van het bestandssysteem is niet opgenomen in de instelling voor schijfcache van de Platform Server. Het totale door het systeem gerapporteerde bedrag kan aanzienlijk hoger zijn dan de instelling. Het wordt aanbevolen om tweemaal zoveel schijfruimte te reserveren als in ` *[!DNL cache.maxSize]*` is opgegeven.

**Gebroken afbeeldingen in de voorbeelden is-docs**

Dit komt voor als de Server van het Beeld niet loopt. Dit gebeurt ook als het hoofdpad van de catalogus of het hoofdpad van de afbeelding is gewijzigd ten opzichte van de standaardinstelling van de installatie, maar de voorbeeldafbeeldingen en catalogi zijn niet naar de nieuwe locaties verplaatst. Controleer de waarde van de Weg van de Weg van de Wortel van de Server van het Beeld in configuratiedossiers. Verplaats zo nodig de demomap met de voorbeeldafbeeldingen naar de huidige hoofdmap van de afbeelding en verplaats [!DNL sample*.*] naar de huidige hoofdmap van de catalogus.

In de voorbeelden wordt ook aangenomen dat bepaalde instellingen in [!DNL default.ini] standaard zijn (zo mag de optie voor verduistering of vergrendeling niet worden ingeschakeld).

**Te veel cachefouten na aanzienlijke uptime**

Afhankelijk van servergebruik, kunnen de prestaties worden verbeterd door de grootte van het geheime voorgeheugen van de Server van het Platform te verhogen als de schijfruimte beschikbaar is. U kunt instellingen wijzigen door configuratiebestanden handmatig te bewerken. Zie documentatie.

**Logbestanden nemen te veel schijfruimte in beslag**

De Server van het Beeld en de Server van het Platform beginnen elke dag een nieuw logboekdossier. Deze worden standaard in [!DNL *[!DNL install_root]*/ImageServing/logs] geplaatst. De bestandsgrootte, het aantal bijgehouden logbestanden en de loginhoud kunnen worden geconfigureerd. Zie documentatie.

**Als u antivirussoftware op de server hebt geïnstalleerd**

U wordt aangeraden het scannen naar mappen met afbeeldingsservices uit te schakelen. Anders kan het scannen van mappen voor lezen/schrijven van grote volumes (zoals cache, afbeeldingen, lettertypen, profielen en catalogusmappen) problemen veroorzaken.

**Digimarc veroorzaakt prestatieproblemen voor zoomafbeeldingen**

Gebruik Digimarc niet voor afbeeldingen waarop wordt ingezoomd. De prestaties zijn niet acceptabel. Maak indien nodig een aparte catalogus voor afbeeldingen die u wilt gebruiken voor zoomen en schakel Digimarc uit voor deze catalogus.
