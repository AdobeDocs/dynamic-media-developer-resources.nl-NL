---
description: Beschrijft de gemeenschappelijke verrichtingsparameters die door de IPS Dienst API van het Web worden behandeld.
solution: Experience Manager
title: Bewerkingsmethoden
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 020c8e63-ad4e-4c0d-8da6-b51efb2b89a5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 0%

---

# Bewerkingsmethoden{#operations-methods}

Deze sectie beschrijft de gemeenschappelijke verrichtingsparameters die door de IPS Dienst API van het Web worden behandeld.

Voor een volledige beschrijving van elke parameter van de verrichting, zie [Operatieparameters](/help/aem-ips-api/operations/c-operations-intro/c-methods/c-methods.md).

## Handgrepen: informatie {#section-094ce1afa6244fa5b2c762f44ffdca1c}

Handelt referentieIPS voorwerpen die door bepaalde API verrichtingen zijn teruggekeerd. U kunt handvatten als parameters tot verdere verrichtingsvraag ook overgaan. Handgrepen zijn typen tekenreeksgegevens ( `xsd:string`).

Handgrepen zijn alleen bedoeld voor gebruik tijdens één toepassingssessie. Voorts zou u handvatten blijvend moeten maken omdat hun formaat tussen IPS versies kan veranderen. Wanneer u interactieve toepassingen schrijft, voert u zittingsonderbrekingen uit en verwerpt alle handvatten tussen zittingen, in het bijzonder na een IPS verbetering. Wanneer u niet-interactieve toepassingen schrijft, roep de aangewezen verrichtingen om handvatten terug te winnen telkens als de toepassing in werking wordt gesteld. De volgende Java/Axis2-codevoorbeelden tonen een onjuiste en correcte uitvoering van de code:

**Onjuiste handlercode**

Dit codevoorbeeld is onjuist omdat het een hard-gecodeerde waarde (555) voor het bedrijfshandvat bevat.

```
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle("555");// INCORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

**Correcte handvatcode**

Deze codesteekproef is correct omdat het roept `getCompanyInfo` om een geldige greep te retourneren. Er wordt geen hard gecodeerde waarde voor gebruikt. Gebruik deze methode-of andere IPS API equivalent-om de vereiste handgreep terug te keren.

```
GetCompanyInfoParam companyInfoParam = new GetCompanyInfoParam(); 
companyInfoParam.setCompanyName("My Company"); GetCompanyInfoReturn companyInfoReturn = ipsApi.getCompanyInfo(companyInfoParam, authHeader); 
String companyHandle = companyInfoReturn.getCompanyInfo().getCompanyHandle(); 
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle(companyHandle); //CORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

## Algemene typen handgrepen {#section-e683ac8283284f9688e63f51a494f7a0}

**companyHandle**

De meeste verrichtingen vereisen u om een bedrijfcontext te plaatsen door in te gaan `companyHandle` parameter. De bedrijfshandgreep is een aanwijzer die wordt geretourneerd door bepaalde bewerkingen, zoals `getCompanyInfo`, `addCompany`, en `getCompanyMembership`.

**userHandle**

De `userHandle` parameter is een optionele parameter voor bewerkingen die op een specifieke gebruiker zijn gericht. Door gebrek, richten deze verrichtingen de roepende gebruiker (de gebruiker waarvan geloofsbrieven binnen voor authentificatie worden overgegaan). Beheerders met de juiste machtigingen kunnen echter een andere gebruiker opgeven. Bijvoorbeeld de `setPassword` bewerking stelt normaal gesproken het wachtwoord van de geverifieerde gebruiker in, maar een beheerder kan de opdracht `userHandle` om het wachtwoord voor een andere gebruiker in te stellen.

Voor verrichtingen die een bedrijfcontext vereisen (het gebruiken van `companyHandle` parameter), zowel moeten de voor authentiek verklaarde als doelgebruikers lid van het gespecificeerde bedrijf zijn. Voor verrichtingen die geen bedrijfcontext vereisen, moeten de voor authentiek verklaarde en doelgebruikers allebei lid van minstens één gemeenschappelijk bedrijf zijn.

De volgende bewerkingen kunnen gebruikershandgrepen ophalen:

* `getUsers`
* `getAllUsers`
* `getUserInfo`
* `getCompanyMembers`
* `getGroupMembers`
* `addUser`

**accessUserHandle en accessGroupHandle**

Door gebrek, werken de verrichtingen die toegangstoestemmingen (lezen, schrijven, schrappen) vereisen in de toestemmingscontext van de roepende gebruiker. Met bepaalde bewerkingen kunt u deze context wijzigen met de `accessUserHandle` of `accessGroupHandle` parameter. De `accessUserHandle` Met parameter kan een beheerder een andere gebruiker nadoen. De `accessGroupHandle` parameter staat de bezoeker toe om in de context van een specifieke gebruikersgroep te werken.

**responseFieldArray en excludeFieldArray**

Met sommige bewerkingen kan de aanroeper beperken welke velden in de reactie worden opgenomen. Door velden te beperken, kunt u de tijd en het geheugen die nodig zijn om de aanvraag te verwerken verminderen en de grootte van de reactiegegevens verminderen. De aanroeper kan om een specifieke lijst van gebieden verzoeken door a over te gaan `responseFieldArray` of met een opgesomde lijst van uitgesloten velden via de `excludeFieldArray` parameter.

Beide `responseFieldArray` en `excludeFieldArray` velden opgeven met behulp van een nodepad gescheiden door `/`. Als u bijvoorbeeld wilt opgeven dat `searchAssets` retourneert alleen de naam, de laatst gewijzigde datum en de metagegevens voor elk element verwijzen naar het volgende:

```
<responseFieldArray> 
   <items>assetArray/items/name</items> 
   <items>assetArray/items/lastModified</items> 
   <items>assetArray/items/metadataArray</items> 
</responseFieldArray>
```

Op dezelfde manier om alle gebieden (behalve toestemmingen) terug te keren:

```
<excludeFieldArray> 
   <items>assetArray/items/permissions</items> 
</excludeFieldArray>
```

Merk op dat de knoopwegen met betrekking tot de wortel van de terugkeerknoop zijn. Als u een complex tekstveld opgeeft zonder subelementen (bijvoorbeeld `assetArray/items/imageInfo`), worden alle subelementen opgenomen. Als u een of meer subelementen opgeeft in een complex tekstveld (bijvoorbeeld `assetArray/items/imageInfo/originalPath`), worden alleen die subelementen opgenomen.

Als u dit niet doet `responseFieldArray` of `excludeFieldArray` in een aanvraag worden alle velden geretourneerd.

**Landinstelling**

Sinds IPS 4.0, steunt IPS API het plaatsen van de scènecontext van een verrichting door over te gaan `authHeader` locale, parameter. Wanneer de parameter locale niet aanwezig is, wordt de HTTP-header `Accept-Language` wordt gebruikt. Als deze kopbal ook niet aanwezig is, wordt de standaardscène voor de IPS server gebruikt.

Bij bepaalde bewerkingen worden ook expliciete landinstellingsparameters gebruikt, die kunnen verschillen van de context van de landinstelling van de bewerking. Bijvoorbeeld de `submitJob` de bewerking neemt een `locale` parameter die de landinstelling instelt die wordt gebruikt voor het vastleggen van taken en e-mailmeldingen.

Landinstellingsparameters gebruiken de indeling `<language_code>[-<country_code>]`

Wanneer de taalcode een kleine letter is, is de tweelettercode volgens ISO-639 en de optionele landcode een hoofdletter, tweelettercode volgens ISO-3266. De landinstelling voor Amerikaans Engels is bijvoorbeeld `en-US`.
