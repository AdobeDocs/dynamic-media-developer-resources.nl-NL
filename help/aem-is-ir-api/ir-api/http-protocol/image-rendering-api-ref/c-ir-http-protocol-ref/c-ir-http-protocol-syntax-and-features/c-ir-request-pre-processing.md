---
description: Rendering van afbeeldingen biedt een eenvoudige aanvraag vooraf processor op basis van regels voor reguliere expressies en substituties.
solution: Experience Manager
title: Voorbewerking aanvragen *
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---


# Voorbewerking aanvragen *{#request-pre-processing}

Rendering van afbeeldingen biedt een eenvoudige aanvraag vooraf processor op basis van regels voor reguliere expressies en substituties.

U kunt verzamelingen van regels (regelsets) toevoegen aan elke materiaalcatalogus, inclusief de standaardcatalogus. Regels worden opgegeven bij bestanden met XML-opmaak.

De pre-verwerkingsregels van het verzoek kunnen de weg en vraaggedeelten verzoeken wijzigen alvorens zij door het Beeld worden verwerkt die parser teruggeeft, met inbegrip van het manipuleren van de weg, het toevoegen van bevelen, het veranderen van bevelwaarden, en het toepassen van malplaatjes of macro&#39;s. De regels kunnen ook worden gebruikt om bepaalde eigenschappen te vormen en met voeten te treden die normaal slechts met catalogusattributen, zoals het plaatsen van de standaard grootte van het antwoordbeeld of het beperken van de dienst van HTTP tot specifieke cliëntIP adressen worden gecontroleerd.

Voorverwerkingsregels voor aanvragen zijn geschikt voor diverse toepassingen, waarvan sommige hieronder worden vermeld:

* Implementeer een *virtueel paden* mechanisme, waarmee het aanvraagpad opnieuw kan worden toegewezen aan bestands-, FTP- en HTTP-paden.
* Het gebruik van CPU-intensieve opdrachten wordt niet toegestaan om servermisbruik te voorkomen.
* De kwaliteitsinstellingen voor afbeeldingen bepalen (zoals JPEG-kwaliteit of verscherpen), afhankelijk van het aanvraagpad of de naam van de afbeelding.

De gedetailleerde informatie over het creëren van, het gebruiken van, en het beheren van regelreeksen kan in de Reeks van de Regel Verwijzing worden gevonden.

Zie ook Referentie voor regelset, kenmerk::RuleSetFile
