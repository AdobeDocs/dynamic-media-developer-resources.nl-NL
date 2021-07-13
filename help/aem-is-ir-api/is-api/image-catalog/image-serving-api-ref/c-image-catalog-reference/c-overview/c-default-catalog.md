---
description: De standaardcatalogus bevat standaardwaarden voor alle cataloguskenmerken van alle afbeeldingscatalogi.
solution: Experience Manager
title: Standaardcatalogus
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: db42fb67-aa6f-4217-bc69-45b01bbd0b10
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---

# Standaardcatalogus{#default-catalog}

De standaardcatalogus bevat standaardwaarden voor alle cataloguskenmerken van alle afbeeldingscatalogi.

Als een bepaald kenmerk niet in een specifieke afbeeldingscatalogus kan worden gevonden, gebruikt de server in plaats daarvan de corresponderende waarde uit de standaardcatalogus. Op dezelfde manier kan de standaardcatalogus worden gebruikt om standaardwaarden te bieden voor specifieke records met catalogusgegevens (afbeeldingen, macrodefinities, lettertypen en ICC-profielen). Als een bepaalde gegevensrecord niet kan worden gevonden in een specifieke afbeeldingscatalogus, probeert de server deze in plaats daarvan te vinden in de standaardcatalogus. Hierdoor kunnen afbeeldingscatalogi dunbevolkt worden en wordt het beheer van algemene kenmerken en gegevens, zoals gedeelde sjablonen, macro&#39;s, lettertypen enzovoort, vereenvoudigd.

Bovendien bevat de standaardcatalogus alle kenmerken en gegevensrecords (macro&#39;s, lettertypen, ICC-profielen, regels voor voorbewerking aanvragen) wanneer een bewerking geen specifieke afbeeldingscatalogus bevat.

Voor een correcte werking van de Server van het Platform moet het dossier van catalogusattributen voor de standaardcatalogus [!DNL default.ini] worden genoemd, altijd in de catalogusomslag bestaan, en moet volledig met alle vereiste attributen, behalve `attribute::RootId` en de verwijzingen naar de diverse dossiers van catalogusgegevens, die allen facultatief zijn worden bevolkt.

>[!NOTE]
>
>Alle cataloguskenmerkbestanden behalve [!DNL default.ini] moeten een unieke `attribute::RootId`-waarde bevatten. `attribute::RootId` in  [!DNL default.ini] moet leeg zijn.
