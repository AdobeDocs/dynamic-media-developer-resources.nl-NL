---
description: Gebruik deze serverinstellingen voor inhoudsgegevensmappen.
solution: Experience Manager
title: Inhoudsgegevensmappen
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9aa4121f-25f8-49d0-a304-7ae756c046f5
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# Inhoudsgegevensmappen{#content-data-folders}

Gebruik deze serverinstellingen voor inhoudsgegevensmappen.

## IS::RootPath - Hoofdmappen met afbeeldingsgegevens {#section-5c57569514bb4d00b19de31d2e137e3b}

De locatie van alle brongegevens, inclusief afbeeldingen, lettertypen en ICC-profielen. Dit kunnen een of meer absolute bestandspaden of paden zijn die relatief zijn ten opzichte van *[!DNL install_folder]*, gescheiden met puntkomma&#39;s. Indien leeg, *[!DNL install_folder]* is de standaardbasis. U kunt meerdere waarden opgeven om afbeeldingsgegevens over meerdere bestandssystemen te verspreiden. De server van het Beeld zal de wortelwegen in de gespecificeerde orde proberen tot het gevraagde dossier wordt gevonden.

## PS::staticContent.rootPath - Static Content Data Root Folders {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

De locatie van statische inhoudsbrongegevens die via de [!DNL /is/static] context. Kan een of meer absolute bestandspaden of paden zijn ten opzichte van *[!DNL install_folder]*, gescheiden met puntkomma&#39;s. Indien leeg, *[!DNL install_folder]* is de standaardbasis.

Meerdere waarden kunnen worden opgegeven, gescheiden door puntkomma&#39;s, om statische inhoud over meerdere bestandssystemen te distribueren. Normaal gesproken op dezelfde waarden ingesteld als `IS::RootPath`.

De [!DNL Platform Server] probeert de wortelwegen in de gespecificeerde orde tot het gevraagde dossier wordt gevonden.

>[!NOTE]
>
>Standaard wordt dit veld opzettelijk ingesteld op een niet-bestaande locatie ( [!DNL *[!DNL install_folder]*/static]), effectief onbruikbaar makend de statische inhoudsdienst.

## IS::Opslagmap - Hoofdmap van bestand opslaan {#section-1c517f8d49ce4cb8b9013e520bf309c9}

Het hoofdpad voor `attribute::SavePath` (wordt gebruikt door `req=saveToFile`). De server van het Beeld moet toegangstoestemmingen voor subfolder tot stand brengen waarin het beelddossiers zal creëren.
