---
title: Tekstreeks lokaliseren
description: Bij de lokalisatie van teksttekenreeksen kunnen afbeeldingscatalogi meerdere landspecifieke representaties voor dezelfde tekenreekswaarde bevatten.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f105c7f2-b544-4c08-bb91-4916e485572d
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 0%

---

# Tekstreeks lokaliseren{#text-string-localization}

Bij de lokalisatie van teksttekenreeksen kunnen afbeeldingscatalogi meerdere landspecifieke representaties voor dezelfde tekenreekswaarde bevatten.

De server geeft de client de representatie weer die overeenkomt met de landinstelling die is opgegeven met `locale=`, het vermijden van lokalisatie aan de clientzijde en het toestaan van toepassingen om landinstellingen eenvoudig te schakelen door de juiste `locale=` waarde met de IS tekstverzoeken.

## Toepassingsgebied {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

Tekstreeklokalisatie wordt toegepast op alle tekenreekselementen die het lokalisatietoken bevatten ` ^loc= *`locId`*^` in de volgende catalogusvelden:

<table id="table_83344EFCB5B5418184E0A0B43D0B23F7"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Catalogusveld</b> </th> 
   <th class="entry"> <b>Tekenreekselement in veld</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> catalogus::ImageSet </span> </p> </td> 
   <td> <p>Elk subelement met een vertaalbare tekenreeks (gescheiden door een combinatie van scheidingstekens ',' ';' ':' en/of het begin/einde van het veld). </p> <p> A <span class="codeph"> 0xrrggbb </span> kleurwaarde aan het begin van een lokaliseerbaar veld wordt niet gelokaliseerd en ongewijzigd doorgegeven. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogus::Kaart </span> </p> </td> 
   <td> <p>Een enkele of dubbele kenmerkwaarde, met uitzondering van de waarden van de <span class="codeph"> coördins= </span> en <span class="codeph"> shape= </span> kenmerken. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogus::doelen </span> </p> </td> 
   <td> <p>De waarde van <span class="codeph"> doel.*.label </span> en <span class="codeph"> doel.*.userdata </span> eigenschap. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogus::UserData </span> </p> </td> 
   <td> <p>De waarde van een eigenschap. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Tekenreekssyntaxis {#section-d12320edf300409f8e17565b143acafc}

Localisatie ingeschakeld *`string`* elementen in de afbeeldingscatalogus bestaan uit een of meer gelokaliseerde tekenreeksen, die elk worden voorafgegaan door een lokalisatietoken.

<table id="simpletable_CEFDAE8395E6493E902D58A7E5A25BC7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> stringElement </span> </span> </p> </td> 
  <td class="stentry"> <p>[ <span class="varname"> defaultString </span>]*{ <span class="varname"> localizationToken </span> <span class="varname"> localizedString </span>} </p> </td> 
 </tr> 
</table>

<table id="simpletable_0A687FA72C4C4C1AAFFCB43143C1AB3B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizationToken </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ^loc= <span class="varname"> locStr </span> ^ </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> locId </span> </span> </p> </td> 
  <td class="stentry"> <p>Interne landinstellings-id voor de <span class="varname"> localizedString </span> volgt <span class="varname"> localizationToken </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizedString </span> </span> </p> </td> 
  <td class="stentry"> <p>Gelokaliseerde tekenreeks </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> defaultString </span> </span> </p> </td> 
  <td class="stentry"> <p>Tekenreeks die moet worden gebruikt voor onbekende landinstellingen. </p> </td> 
 </tr> 
</table>

De *`locId`* moet ASCII zijn en mag geen &#39;^&#39; bevatten.

&#39;^&#39; kan overal in substrings met of zonder HTTP-codering voorkomen. De server komt overeen met het volledige *`localizationToken`* `^loc=locId^` patroon om subtekenreeksen te scheiden.

De *`stringElements`*, die niet ten minste één *`localizationToken`*, niet in aanmerking worden genomen voor lokalisatie.

## De vertaalkaart {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap` bepaalt de regels die door de server worden gebruikt om te bepalen welke *`localizedStrings`* om terug te keren naar de client. Het bestaat uit een lijst met invoer *`locales`* (die overeenkomen met de waarden die zijn opgegeven met `locale=`), elk met geen of meer interne id&#39;s voor landinstellingen ( *`locId`*). Bijvoorbeeld:

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

Leeg *`locId`* waarden geven aan dat de *`defaultString`* moet worden teruggegeven, indien beschikbaar.

Zie de beschrijving van `attribute::LocaleStrMap` voor meer informatie.

## Het vertaalproces {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

Op basis van het bovenstaande voorbeeld en de aanvraag `/is/image/myCat/myItem?req=&locale=nl`, zoekt de server eerst naar &quot; `nl`&quot; in de landinstellingskaart. De overeenkomende vermelding `nl,N` geeft aan dat voor elk *`stringElement`* de *`localizedString`* gemarkeerd `^loc=N^` moeten worden geretourneerd. Als dit *`localizationToken`* niet aanwezig is in de *`stringElement`*, wordt een lege waarde geretourneerd.

Laten we zeggen `catalog::UserData` for `myCat/myItem` bevat het volgende (voor de duidelijkheid worden regeleinden ingevoegd):

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

De server retourneert het volgende in reactie op de voorbeeldaanvraag:

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## Onbekende landinstellingen {#section-26dfeefbd60345de94bbfeaaf7741223}

In het bovenstaande voorbeeld: `attribute::LocaleStrMap` heeft een item met een lege waarde *`locale`* waarde. De server gebruikt deze vermelding om alles te verwerken `locale=` waarden die niet uitdrukkelijk anders in de vertaalkaart worden gespecificeerd.

In het voorbeeld van de vertaalkaart wordt aangegeven dat in een dergelijk geval *`defaultString`* moet worden teruggegeven, indien beschikbaar. Daarom is het volgende teruggekeerd als deze vertaalkaart op het verzoek wordt toegepast `/is/image/myCat/myItem?req=&locale=ja`:

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## Voorbeelden {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**Talenfamilies**

Meerdere *`locId`* waarden kunnen aan elk *`locale`* in de vertaalkaart. De reden is dat het ondersteuning van landspecifieke of regiospecifieke variaties (bijvoorbeeld Engels in de VS versus Engels in het Verenigd Koninkrijk) toestaat voor selectie *`stringElements`* bij het verwerken van de meeste inhoud met gangbare basislandinstellingen (bijvoorbeeld Internationaal Engels).

Ondersteuning wordt bijvoorbeeld toegevoegd voor Amerikaans-specifiek Engels ( `*`locId`* EUS`) en het VK-specifieke Engels ( `*`locId`* EUK`), om de af en toe alternatieve spelling te ondersteunen. Indien EUK of EUS niet bestaat, valt dit terug op E. Evenzo komen Oostenrijkse specifieke Duitse varianten ( `DAT`) indien nodig beschikbaar worden gesteld bij de terugkeer van het Duits *`localizedStrings`* (gemarkeerd met `D`) meestal.

De `attribute::LocaleStrMap` zou er als volgt uitzien:

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

In de volgende tabel wordt de uitvoer voor een vertegenwoordiger beschreven *`stringElement`* en *`locale`* combinaties:

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
   <td> <p> <span class="codeph"> ^loc=E^English^loc=D^German </span> </p> </td> 
   <td> <p> en, en_us, en_uk </p> <p> de, de_at, de_de </p> <p>alle andere </p> </td> 
   <td> <p>Engels </p> <p>Duits </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=UKE^UK-English^loc=D^German^loc=DAT^Austrian </span> </p> </td> 
   <td> <p> en, en_us </p> <p> en_uk </p> <p> de, de </p> <p>de_at </p> <p>alle andere </p> </td> 
   <td> <p>Engels </p> <p>Engels (GB) </p> <p>Duits </p> <p>Oostenrijks </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^ loc=en^English^loc=USE^US-English^loc=D^German^loc=DDE^Deutsch </span> </p> <p> In dit voorbeeld wordt <span class="varname"> locId </span> DDE bestaat niet in <span class="codeph"> kenmerk:LocaleStrMap </span>en dus de subtekenreeks die aan deze eigenschap is gekoppeld <span class="varname"> locId </span> wordt nooit geretourneerd. </p> </td> 
   <td> <p> en, en_uk </p> <p> nl_NL </p> <p> de, de_at, de_de </p> <p>alle andere </p> </td> 
   <td> <p>Engels </p> <p>US-English </p> <p>Duits </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>
