---
description: Beschrijft de gemeenschappelijke verrichtingsparameters die door de IPS Dienst API van het Web worden behandeld.
solution: Experience Manager
title: Bewerkingsmethoden
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 0%

---


# Bewerkingsmethoden{#operations-methods}

Deze sectie beschrijft de gemeenschappelijke verrichtingsparameters die door de IPS Dienst API van het Web worden behandeld.

Zie [Operatieparameters](/help/aem-ips-api/operations/c-operations-intro/c-methods/c-methods.md) voor een volledige beschrijving van elke bewerkingsparameter.

## Handgrepen: Info {#section-094ce1afa6244fa5b2c762f44ffdca1c}

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

Deze codesteekproef is correct omdat het `getCompanyInfo` roept om geldige handvat terug te keren. Er wordt geen hard gecodeerde waarde voor gebruikt. Gebruik deze methode-of andere IPS API equivalent-om de vereiste handgreep terug te keren.

```
GetCompanyInfoParam companyInfoParam = new GetCompanyInfoParam(); 
companyInfoParam.setCompanyName("My Company"); GetCompanyInfoReturn companyInfoReturn = ipsApi.getCompanyInfo(companyInfoParam, authHeader); 
String companyHandle = companyInfoReturn.getCompanyInfo().getCompanyHandle(); 
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle(companyHandle); //CORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

## Algemene handvattypen {#section-e683ac8283284f9688e63f51a494f7a0}

**companyHandle**

De meeste verrichtingen vereisen u om een bedrijfcontext te plaatsen door in een `companyHandle` parameter over te gaan. De bedrijfshandgreep is een aanwijzer die wordt geretourneerd door bepaalde bewerkingen, zoals `getCompanyInfo`, `addCompany` en `getCompanyMembership`.

**userHandle**

De parameter `userHandle` is een optionele parameter voor bewerkingen die een specifieke gebruiker als doel hebben. Door gebrek, richten deze verrichtingen de roepende gebruiker (de gebruiker waarvan geloofsbrieven binnen voor authentificatie worden overgegaan). Beheerders met de juiste machtigingen kunnen echter een andere gebruiker opgeven. De bewerking `setPassword` stelt bijvoorbeeld normaal het wachtwoord van de geverifieerde gebruiker in, maar een beheerder kan de parameter `userHandle` gebruiken om het wachtwoord voor een andere gebruiker in te stellen.

Voor verrichtingen die een bedrijfcontext (gebruikend de `companyHandle` parameter) vereisen, zowel moeten de voor authentiek verklaarde als doelgebruikers lid van het gespecificeerde bedrijf zijn. Voor verrichtingen die geen bedrijfcontext vereisen, moeten de voor authentiek verklaarde en doelgebruikers allebei lid van minstens één gemeenschappelijk bedrijf zijn.

De volgende bewerkingen kunnen gebruikershandgrepen ophalen:

* `getUsers`
* `getAllUsers`
* `getUserInfo`
* `getCompanyMembers`
* `getGroupMembers`
* `addUser`

**accessUserHandle en accessGroupHandle**

Door gebrek, werken de verrichtingen die toegangstoestemmingen (lezen, schrijven, schrappen) vereisen in de toestemmingscontext van de roepende gebruiker. Met bepaalde bewerkingen kunt u deze context wijzigen met de parameter `accessUserHandle` of `accessGroupHandle`. Met de parameter `accessUserHandle` kan een beheerder een andere gebruiker nadoen. De `accessGroupHandle` parameter staat de bezoeker toe om in de context van een specifieke gebruikersgroep te werken.

**responseFieldArray en excludeFieldArray**

Met sommige bewerkingen kan de aanroeper beperken welke velden in de reactie worden opgenomen. Door velden te beperken, kunt u de tijd en het geheugen die nodig zijn om de aanvraag te verwerken verminderen en de grootte van de reactiegegevens verminderen. De aanroeper kan om een specifieke lijst van gebieden verzoeken door een `responseFieldArray` parameter, of met een opgesomde lijst van uitgesloten gebieden via de `excludeFieldArray` parameter over te gaan.

Zowel `responseFieldArray` als `excludeFieldArray` specificeren gebieden door een knoopweg te gebruiken die door `/` wordt gescheiden. Als u bijvoorbeeld wilt opgeven dat `searchAssets` alleen de naam, de laatst gewijzigde datum retourneert en de metagegevens voor elk element verwijzen naar het volgende:

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

Merk op dat de knoopwegen met betrekking tot de wortel van de terugkeerknoop zijn. Als u een complex typeveld zonder om het even welke sub-elementen (bijvoorbeeld, `assetArray/items/imageInfo`) specificeert, dan zijn alle sub-elementen inbegrepen. Als u een of meer subelementen opgeeft in een complex tekstveld (bijvoorbeeld `assetArray/items/imageInfo/originalPath`), worden alleen die subelementen opgenomen.

Als u `responseFieldArray` of `excludeFieldArray` niet opneemt in een verzoek, worden alle gebieden teruggekeerd.

**Landinstelling**

Sinds IPS 4.0, steunt IPS API het plaatsen van de scènecontext van een verrichting door de `authHeader` scèneparameter over te gaan. Als de parameter locale niet aanwezig is, wordt de HTTP-header `Accept-Language` gebruikt. Als deze kopbal ook niet aanwezig is, zal de standaardscène voor de IPS server worden gebruikt.

Bij bepaalde bewerkingen worden ook expliciete landinstellingsparameters gebruikt, die mogelijk anders zijn dan de context van de landinstelling van de bewerking. Voor de bewerking `submitJob` wordt bijvoorbeeld een parameter `locale` gebruikt die de landinstelling instelt die wordt gebruikt voor het vastleggen van taken en e-mailmeldingen.

Landinstellingsparameters gebruiken de notatie `<language_code>[-<country_code>]`

Wanneer de taalcode een kleine letter is, is de tweelettercode volgens ISO-639 en de optionele landcode een hoofdletter, tweelettercode volgens ISO-3266. De landinstelling voor Amerikaans Engels is bijvoorbeeld `en-US`.
