---
description: De ingangen van het geheime voorgeheugen worden automatisch verfrist gebruikend of op catalogus-gebaseerde of op afloop-gebaseerde geheim voorgeheugenbevestiging, zoals geselecteerd met attribuut CacheValidationPolicy (in default.ini of het .ini dossier van een specifieke beeldcatalogus).
solution: Experience Manager
title: Validatie van responscache
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d2baa6e6-2700-450f-af1e-88b6d33d0e0c
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---

# Validatie van responscache{#response-cache-validation}

Cachingangen worden automatisch vernieuwd met behulp van op een catalogus gebaseerde of op een vervaldatum gebaseerde cachevalidatie, zoals geselecteerd met kenmerk::CacheValidationPolicy (in default.ini of het .ini-bestand van een specifieke afbeeldingscatalogus).

Bij validatie op basis van een catalogus wordt een bestaand cacheitem als &#39;stable&#39; beschouwd als `catalog::LastModified` (of `attribute::LastModified`of de tijd van de bestandswijziging van de [!DNL catalog.ini] bestand) is recenter dan de tijd waarop de cachevermelding is gemaakt.

Bij validatie op basis van vervaldatum wordt een cacheitem na 5 minuten sinds de meest recente validatie standaard verouderd. In beide gevallen valideert de server de items in de oude cache door de bestandsdatums te controleren van alle afbeeldingsbestanden die bij het maken van de aanvraag betrokken waren. Als de bestandsdatums niet zijn gewijzigd, wordt het tijdstempel van het cacheitem bijgewerkt en wordt de datum in de cache als geldig beschouwd.

Voor gangbare toepassingen waarbij vooral afbeeldingen in afbeeldingscatalogi worden opgenomen, biedt validatie op basis van catalogus een prestatievoordeel. Toepassingen die geen afbeeldingscatalogi bevatten, moeten op vervaldatum gebaseerde cachevalidatie gebruiken. Een manier om dit te bereiken is het instellen van `attribute::cacheValidationPolicy=0` in [!DNL default.ini]en `1` in alle specifieke afbeeldingscatalogusbestanden.

De ingangen van het geheime voorgeheugen worden ongeldig en zijn onderworpen aan re-generatie wanneer een catalogusingang betrokken bij het verzoek op een manier verandert die waarschijnlijk een verandering van het antwoordbeeld zou veroorzaken. De inhoud van bijvoorbeeld `catalog::Modifier` wijzigingen.

>[!NOTE]
>
>Bij Dynamic Media PTIFF-afbeeldingen (piramid TIFF) wordt de bestandsdatum intern in de bestandsheader bewaard voor validatiedoeleinden. De wijzigingstijd van het bestand die door het bestandssysteem wordt aangehouden, wordt gebruikt om te controleren of een niet-PTIFF-bestand is gewijzigd.

Alleen afbeeldingsbestanden nemen deel aan het validatieproces van de cache. Wijzigingen in lettertypebestanden of ICC-profielbestanden leiden niet tot automatische ongeldigmaking van cachegegevens.
