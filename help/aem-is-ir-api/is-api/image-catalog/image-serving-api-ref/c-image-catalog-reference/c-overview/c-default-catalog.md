---
description: De standaardcatalogus bevat standaardwaarden voor alle cataloguskenmerken van alle afbeeldingscatalogi.
solution: Experience Manager
title: Standaardcatalogus
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: db42fb67-aa6f-4217-bc69-45b01bbd0b10
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# Standaardcatalogus{#default-catalog}

De standaardcatalogus bevat standaardwaarden voor alle cataloguskenmerken van alle afbeeldingscatalogi.

Als een bepaald kenmerk niet in een specifieke afbeeldingscatalogus kan worden gevonden, gebruikt de server in plaats daarvan de corresponderende waarde uit de standaardcatalogus. Op dezelfde manier kan de standaardcatalogus worden gebruikt om standaardwaarden te bieden voor specifieke records met catalogusgegevens (afbeeldingen, macrodefinities, lettertypen en ICC-profielen). Als een bepaalde gegevensrecord niet kan worden gevonden in een specifieke afbeeldingscatalogus, probeert de server deze in plaats daarvan te vinden in de standaardcatalogus. Hierdoor kunnen afbeeldingscatalogi dunbevolkt worden en wordt het beheer van algemene kenmerken en gegevens, zoals gedeelde sjablonen, macro&#39;s, lettertypen enzovoort, vereenvoudigd.

Bovendien bevat de standaardcatalogus alle kenmerken en gegevensrecords (macro&#39;s, lettertypen, ICC-profielen, regels voor voorbewerking aanvragen) wanneer een bewerking geen specifieke afbeeldingscatalogus bevat.

Voor een correcte werking van de [!DNL Platform Server] het bestand met cataloguskenmerken voor de standaardcatalogus moet een naam hebben [!DNL default.ini], moet altijd in de catalogusmap staan en moet volledig zijn gevuld met alle vereiste kenmerken, met uitzondering van `attribute::RootId` en de verwijzingen naar de verschillende dossiers van catalogusgegevens, die allen facultatief zijn.

>[!NOTE]
>
>Alle cataloguskenmerkbestanden behalve [!DNL default.ini] moet een unieke `attribute::RootId` waarde. `attribute::RootId` in [!DNL default.ini] moet leeg zijn.
