---
description: Bij lokalisatie van tekstreeksen kunnen afbeeldingscatalogi meerdere landspecifieke representaties voor dezelfde tekenreekswaarde bevatten.
seo-description: Bij lokalisatie van tekstreeksen kunnen afbeeldingscatalogi meerdere landspecifieke representaties voor dezelfde tekenreekswaarde bevatten.
seo-title: Tekstreeks lokaliseren
solution: Experience Manager
title: Tekstreeks lokaliseren
topic: Scene7 Image Serving - Image Rendering API
uuid: bdff2403-e3bb-4b3f-a8d7-bb108c1fbee8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 0%

---


# Tekstreeks lokaliseren{#text-string-localization}

Bij lokalisatie van tekstreeksen kunnen afbeeldingscatalogi meerdere landspecifieke representaties voor dezelfde tekenreekswaarde bevatten.

De server geeft de representatie die overeenkomt met de landinstelling die is opgegeven met `locale=`, terug naar de client, waarbij lokalisatie op de client wordt vermeden en toepassingen de mogelijkheid krijgen om eenvoudig van landinstelling te wisselen door de juiste `locale=`-waarde te verzenden met de IS-tekstaanvragen.

## Toepassingsgebied {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

Tekstreeklokalisatie wordt toegepast op alle tekenreekselementen die het lokalisatietoken ` ^loc= *`locId`*^` in de volgende catalogusvelden bevatten:

<table id="table_83344EFCB5B5418184E0A0B43D0B23F7"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Catalogusveld</b> </th> 
   <th class="entry"> <b>Tekenreekselement in veld</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> catalogus::ImageSet  </span> </p> </td> 
   <td> <p>Een subelement dat een vertaalbare tekenreeks bevat (gescheiden door een combinatie van scheidingstekens ',' ';' ':' en/of het begin/einde van het veld). </p> <p> Een <span class="codeph"> 0xrrggbb </span> kleurwaarde aan het begin van een lokaliseerbaar veld wordt uitgesloten van lokalisatie en wordt ongewijzigd doorgegeven. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogus::Kaart  </span> </p> </td> 
   <td> <p>Een enkele of dubbele kenmerkwaarde, behalve de waarden van de <span class="codeph"> coördins= </span> en <span class="codeph"> shape= </span> attributen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogus::doelen  </span> </p> </td> 
   <td> <p>De waarde van een <span class="codeph">-doel.*.label </span> en <span class="codeph"> doel.*.userdata </span> property. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogus::UserData  </span> </p> </td> 
   <td> <p>De waarde van een eigenschap. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Tekensyntaxis {#section-d12320edf300409f8e17565b143acafc}

Voor lokalisatie geschikte *`string`*-elementen in de afbeeldingscatalogus bestaan uit een of meer gelokaliseerde tekenreeksen, elk voorafgegaan door een lokalisatietoken.

<table id="simpletable_CEFDAE8395E6493E902D58A7E5A25BC7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> stringElement  </span> </span> </p> </td> 
  <td class="stentry"> <p>[ <span class="varname"> defaultString </span>]*{ <span class="varname"> localizationToken </span> <span class="varname"> localizedString </span> </p> </td> 
 </tr> 
</table>

<table id="simpletable_0A687FA72C4C4C1AAFFCB43143C1AB3B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizationToken  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ^loc=  <span class="varname"> locStr  </span> ^  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> locId  </span> </span> </p> </td> 
  <td class="stentry"> <p>Interne landinstellings-id voor de <span class="varname"> gelokaliseerde tekenreeks </span> volgend op deze <span class="varname"> lokalisatietoken </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizedString  </span> </span> </p> </td> 
  <td class="stentry"> <p>Gelokaliseerde tekenreeks. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> defaultString  </span> </span> </p> </td> 
  <td class="stentry"> <p>Tekenreeks die moet worden gebruikt voor onbekende landinstellingen. </p> </td> 
 </tr> 
</table>

*`locId`* moet ASCII zijn en mag geen &#39;^&#39; bevatten.

&#39;^&#39; kan overal voorkomen in subtekenreeksen met of zonder HTTP-codering. De server past het gehele *`localizationToken`* `^loc=locId^` patroon aan afzonderlijke subtekenreeksen aan.

*`stringElements`* die niet ten minste één code bevatten,  *`localizationToken`* worden niet in aanmerking genomen voor lokalisatie.

## De vertaalkaart {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap` bepaalt de regels die door de server worden gebruikt om te bepalen welke  *`localizedStrings`* aan de cliënt terug te keren. Deze bestaat uit een lijst met invoer *`locales`* (die overeenkomt met de waarden opgegeven met `locale=`), elk met geen of meer interne id&#39;s voor landinstellingen ( *`locId`*). Bijvoorbeeld:

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

Lege *`locId`* waarden geven aan dat *`defaultString`* moet worden geretourneerd, indien beschikbaar.

Raadpleeg de beschrijving van `attribute::LocaleStrMap` voor meer informatie.

## Het vertaalproces {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

Op basis van de bovenstaande voorbeeld-vertaalkaart en de aanvraag `/is/image/myCat/myItem?req=&locale=nl` zoekt de server eerst naar &quot; `nl`&quot; in de landinstellingskaart. De overeenkomende vermelding `nl,N` geeft aan dat voor elke *`stringElement`* de *`localizedString`* gemarkeerd met `^loc=N^` moet worden geretourneerd. Als *`localizationToken`* niet aanwezig in *`stringElement`* is, is een lege waarde teruggekeerd.

`catalog::UserData` voor `myCat/myItem` bevat het volgende (voor de duidelijkheid worden regeleinden ingevoegd):

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

De server retourneert het volgende in reactie op ons voorbeeldverzoek:

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## Onbekende landinstellingen {#section-26dfeefbd60345de94bbfeaaf7741223}

In het bovenstaande voorbeeld heeft `attribute::LocaleStrMap` een item met een lege *`locale`*-waarde. De server gebruikt deze vermelding om alle `locale=`-waarden af te handelen die niet expliciet anders in de vertaalkaart zijn opgegeven.

In het voorbeeld van de vertaalkaart wordt aangegeven dat in een dergelijk geval de *`defaultString`* moet worden geretourneerd, indien beschikbaar. Het volgende wordt dus geretourneerd als deze vertaalkaart wordt toegepast op het verzoek `/is/image/myCat/myItem?req=&locale=ja`:

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## Voorbeelden {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**Talenfamilies**

Er kunnen meerdere *`locId`* waarden worden gekoppeld aan elke *`locale`* in de vertaalkaart. Hierdoor kunnen landspecifieke of regiospecifieke variaties (bijvoorbeeld Engels in de VS versus Engels in het Verenigd Koninkrijk) voor het selecteren van *`stringElements`* worden ondersteund, terwijl de meeste inhoud wordt afgehandeld met algemene basislandinstellingen (bijvoorbeeld internationaal Engels).

Voor ons voorbeeld, willen wij steun voor V.S.-specifiek Engels ( ` *`locId`* EUS`) en UK-specifiek Engels ( ` *`locId`* EUK`) toevoegen, om de af en toe alternatieve spelling te steunen. Als EUK of EUS niet bestaat, zouden we terugvallen op E. Op dezelfde manier zouden Oostenrijkse specifieke Duitse varianten ( `DAT`) waar nodig beschikbaar kunnen worden gesteld terwijl het terugkeren van gemeenschappelijk Duits *`localizedStrings`* (gemerkt met `D`) meestal.

`attribute::LocaleStrMap` zou er als volgt uitzien:

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

In de volgende tabel wordt de uitvoer beschreven voor een aantal representatieve combinaties *`stringElement`* en *`locale`*:

<table id="table_A6B67587C5F44B5E9CD0E7ED29A81198"> 
 <thead> 
  <tr> 
   <th class="entry"> <i>stringElement</i> </th> 
   <th class="entry"> <i>landinstelling</i> </th> 
   <th class="entry"> <p>Uitvoertekenreeks </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=D^German  </span> </p> </td> 
   <td> <p> en, en_us, en_uk </p> <p> de, de_at, de_de </p> <p>alle andere </p> </td> 
   <td> <p>Engels </p> <p>Duits </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=UKE^UK-English^loc=D^German^loc=DAT^Austrian  </span> </p> </td> 
   <td> <p> en, en_us </p> <p> en_uk </p> <p> de, de_de </p> <p>de_at </p> <p>alle andere </p> </td> 
   <td> <p>Engels </p> <p>Engels (GB) </p> <p>Duits </p> <p>Oostenrijks </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^ loc=en^English^loc=USE^US-English^loc=D^German^loc=DDE^Deutsch  </span> </p> <p> Merk op dat voor dit voorbeeld <span class="varname"> locId </span> DDE niet in <span class="codeph"> attributen bestaat::LocaleStrMap </span>, en zo wordt het subkoord verbonden aan <span class="varname"> locId </span> nooit teruggekeerd. </p> </td> 
   <td> <p> en, en_uk </p> <p> nl_nl </p> <p> de, de_at, de_de </p> <p>alle andere </p> </td> 
   <td> <p>Engels </p> <p>US-English </p> <p>Duits </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>

