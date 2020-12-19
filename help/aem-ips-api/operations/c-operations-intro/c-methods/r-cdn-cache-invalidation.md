---
description: Hiermee wordt de opgegeven lijst met URL's doorgestuurd naar de Scene7 CDN-provider (Content Distribution Network) om de bestaande cache met HTTP-reacties ongeldig te maken.
seo-description: Hiermee wordt de opgegeven lijst met URL's doorgestuurd naar de Scene7 CDN-provider (Content Distribution Network) om de bestaande cache met HTTP-reacties ongeldig te maken.
seo-title: cdnCacheInvalidation
solution: Experience Manager
title: cdnCacheInvalidation
topic: Scene7 Image Production System API
uuid: 16cf53d4-4101-405c-b008-009b6ac62169
translation-type: tm+mt
source-git-commit: aa095022d43db4bf815aece9bc2b087c53a64e1b
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 0%

---


# cdnCacheInvalidation{#cdncacheinvalidation}

Hiermee wordt de opgegeven lijst met URL&#39;s doorgestuurd naar de Scene7 CDN-provider (Content Distribution Network) om de bestaande cache met HTTP-reacties ongeldig te maken.

## cdnCacheInvalidation: Info {#section-4f70d2bc79d64288b961836ab17e9690}

De CDN geheim voorgeheugenongeldigverklaring dwingt alle HTTP- verzoeken om deze URLs tegen de huidige gepubliceerde gegevens op het netwerk van Scene7 opnieuw te worden bevestigd zodra dit ongeldigingsverzoek door het netwerk CDN wordt verwerkt. URL&#39;s die niet zijn verbonden met de URL-structuur van de Scene7-service en die direct overeenkomen met de hoofdid van het Scene7-bedrijf die is toegewezen op het moment dat het bedrijf wordt gemaakt, resulteren in een API-fout voor de gehele aanvraag. Eventuele ongeldige URL&#39;s die de CDN niet ondersteunt en die als ongeldig worden beschouwd, resulteren ook in een API-fout voor de gehele aanvraag.

**Gebruiksfrequentie: Regels**

De regels die de frequentie van het gebruik van deze eigenschap bepalen worden gecontroleerd door de partners CDN van Scene7. CDN behoudt de discretie om de ontvankelijkheid van deze ongeldig wordingen te degraderen om optimale prestaties van zijn dienst aan zijn gebruikers te handhaven. Mocht Scene7 op de hoogte worden gesteld van het overgebruik van deze functie, dan moeten we de functie uitschakelen, per bedrijf of volledig in de service.

**Bevestigingse-mails**

Bevestigingse-mails van de Scene7 CDN-partner kunnen worden verzonden naar de maker van de lijst of naar maximaal vijf andere e-mailadressen. De API verzendt de bevestiging wanneer het volledige CDN-netwerk op de hoogte is gebracht van het feit dat de URL&#39;s waarnaar in de e-mail wordt verwezen, zijn gewist. Één enkele vraag aan `cdnCacheInvalidation` kan veelvoudige e-mail verzenden als het aantal geleverde URLs het aantal overschrijdt dat Scene7 aan de partner CDN op één enkel bericht kan leveren. Momenteel, zou dat zijn als het verzoek 100 URLs overschrijdt, maar is onderworpen aan verandering die op verzoek van de partner CDN wordt gebaseerd.

**Ondersteund sinds**

6,0

## Toegestane gebruikerstypen {#section-0d7895e733d54fb68beb8d231a04e4c9}

* `IpsAdmin`
* `IpsCompanyAdmin`

## Parameters {#section-bd1ed2b7419945d19a2ebd5668499f72}

**Input** (  `cdnCacheInvalidationParam`)

<table id="table_EDD1875264C846BE951869D528A90D73"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Naam</b> </th> 
   <th class="entry"> <b> Type</b> </th> 
   <th class="entry"> <b> Vereist</b> </th> 
   <th class="entry"> <b> Beschrijving</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> xsd:tekenreeks</span> </p> </td> 
   <td> <p> Ja </p> </td> 
   <td> <p> De handgreep van het bedrijf dat verbonden is met de URL's om ongeldig te maken. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> urlArray</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> types:UrlArray</span> </p> </td> 
   <td> <p> Ja </p> </td> 
   <td> <p> Lijst met maximaal 1000 URL's die ongeldig moeten worden gemaakt in de CDN-cache. Alle URL's moeten de hoofdmapid van het Scene7-bedrijf bevatten om ongeldig te worden gemaakt. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output**(  `cdnCacheInvalidationReturn`)

<table id="table_1D947C1BF8864820AD7BA0CDC0F076F9"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Naam</b> </th> 
   <th class="entry"> <b> Type</b> </th> 
   <th class="entry"> <b> Vereist</b> </th> 
   <th class="entry"> <b> Beschrijving</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> invalidationHandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:tekenreeks</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Een handgreep die verwijst naar het verwijderingsverzoek. </p> <p>De <span class="codeph"> cdnCacheInvalidation</span> API maakt de cache nu bijna onmiddellijk (~5 seconden) ongeldig. Daarom is opiniepeiling voor de status van ongeldigmaking over het algemeen niet langer vereist. </p> 
    <!--<p>The next three paragraphs were added as per CQDOC-13840 With the migration from Akamai v2 API's to fast purge, purging time is now approximately 5 seconds. You are no longer required to poll on the purge URL to find out the status of the purge request.</p>--> 
    <!--<p>The cache invalidation handle used to contained the company ID, the user account type used (small or large), and the purge url. With the release of 2019R1, <codeph>invalidationHandle</codeph> now contains just the company ID and the purge ID. </p>--> 
    <!--<p>Prior to 2019R1, two different Akamai users were being used for each geography (for example, <codeph>cdninvalidatesmallemea</codeph> and <codeph>cdninvalidatelargeemea</codeph>) to invalidate requests, depending on the number of URLs in each request. This functionality was done so that a small request was not blocked because of a large request. Now, with fast purge in 2019R1, the purge is nearly instantaneous, two users are no longer needed, and only one account is used. </p>--> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> estimatedSeconds</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Geschatte seconden tot voltooiing van het verwijderingsverzoek. Clients moeten op dit moment wachten voordat ze de opiniepeilingstatus hebben. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Voorbeeld {#section-f414361a58e84dfcbbac30a358d02125}

In dit voorbeeld worden vier URL&#39;s ongeldig gemaakt in de CDN-cache. De reactie bevat summiere tellingen van het succes van de verrichtingen en een lijst van foutendetails die direct van CDN worden geleverd om de cliënt in gebruik van deze eigenschap bij te staan.

`getCdnCacheInvalidationStatus` bewerking.

**Verzoek**

```java
<cdnCacheInvalidationParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-02-14">
   <companyHandle>c|6</companyHandle>
   <urlArray>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/11008047?$thumbnail$</items>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/11008047?$product$</items>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/11008047?$large$</items>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/ImageSetConfigDefaults?req=userdata</items>
    </urlArray>
</cdnCacheInvalidationParam>
```

**Antwoord**

```java
<cdnCacheInvalidationReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-02-14">
   <successCount>4</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</cdnCacheInvalidationReturn>
```

