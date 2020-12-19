---
description: Gebruik deze serverinstellingen voor het aanmelden van toegang.
seo-description: Gebruik deze serverinstellingen voor het aanmelden van toegang.
seo-title: Toegangslogbestand
solution: Experience Manager
title: Toegangslogbestand
topic: Scene7 Image Serving - Image Rendering API
uuid: ea7d5d39-3f0a-45f0-bc28-6828a9c9da50
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 0%

---


# Toegangslogbestand{#access-logging}

Gebruik deze serverinstellingen voor het aanmelden van toegang.

Syntaxis

## TC::directory - Logbestandsmap {#section-5d9e2168d4504bbe9868b7d6051c9d67}

De map waarnaar de server van het Platform logbestanden schrijft. Dit kan een absoluut pad zijn of een pad ten opzichte van *`install_folder`*. Standaard is [!DNL  *`install_folder`*/logs].

>[!NOTE]
>
>U moet de nieuwe map maken voordat u deze instelling wijzigt. Zorg ervoor dat de map de juiste lees-/schrijftoegangsrechten heeft als Image Serving is geïnstalleerd om te worden uitgevoerd onder een andere gebruikersaccount dan de hoofdmap.

## TC::maxDays - Aantal dagen om logbestanden bij te houden {#section-45cbecffc5694c87b7d5c176a44a4885}

Het aantal dagen dat logbestanden moeten worden bewaard. De nieuwe logboekdossiers worden gecreeerd elke dag om middernacht. Op dit ogenblik, zal de server alle dossiers in de omslag van het logboekdossier schrappen die ouder zijn dan het gespecificeerde aantal dagen, met inbegrip van die geschreven door de Server van het Beeld of de Server van de Render. De standaardwaarde is 10.

## TC::voorvoegsel - Naam toegangslogbestand {#section-1003856323b844049632710a5a056aa7}

Het voorvoegsel van de naam voor het bestand waarnaar de gegevens van het toegangslogboek worden geschreven. De datum en het dossierachtervoegsel ( [!DNL  *`yyyy`*-*`mm`*-*`dd`*.log]) worden toegevoegd aan het gespecificeerde koord. De naam van het toegangslogboekdossier moet van dat van het dossier van het spoorlogboek verschillend zijn. De standaardwaarde is &quot; `access-`&quot;.

## TC::patroon - Toegangslogpatroon {#section-22775ea85cee444d8a7d7336a3b1feef}

Specificeert het gegevenspatroon voor de verslagen van het de toegangslogboek van de Server van het Platform. De patroontekenreeks geeft variabelen op die worden vervangen door de overeenkomende waarden. Alle andere tekens in de patroontekenreeks worden letterlijk overgedragen naar de logrecord.

Als u het opwarmhulpprogramma voor cache wilt gebruiken, moeten spaties worden gebruikt als veldscheidingstekens. De server van het Platform vervangt alle ruimten en &quot;%&quot;karakters in gebiedswaarden door `%20` en `%25`, respectievelijk.

De volgende patroonvariabelen worden ondersteund:

<table id="table_7A07AFF34B5040A5B30F5735CFE9428F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Patroon</b> </th> 
   <th class="entry"> <b>Beschrijving</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> %a  </span> </p> </td> 
   <td> <p>Extern IP-adres. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %A  </span> </p> </td> 
   <td> <p>Lokaal IP-adres. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %b  </span> </p> </td> 
   <td> <p>Aantal bytes van de reactie exclusief HTTP- kopballen, of " als nul. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %B  </span> </p> </td> 
   <td> <p>Aantal responbytes exclusief HTTP-headers. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %D  </span> </p> </td> 
   <td> <p>Verwerkingstijd aanvragen in milliseconden. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %I  </span> </p> </td> 
   <td> <p>thread id (voor kruisverwijzingen naar logitems voor foutopsporing/fout). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %G  </span> </p> </td> 
   <td> <p>datum en tijd, opgemaakt als <span class="codeph"> <span class="varname"> jjjj </span>- <span class="varname"> MM </span>- <span class="varname"> dd </span> <span class="varname"> HH </span>: <span class="varname"> mm </span>: <span class="varname"> ss </span>. <span class="varname"> SSS- </span> verschuiving  </span> </p> <p> ( <span class="varname"> SSS </span> zijn msec, <span class="varname"> verschuiving </span> is de GMT-tijdverschuiving); de tijdwaarde wordt vastgelegd wanneer de reactie naar de client wordt verzonden. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %m  </span> </p> </td> 
   <td> <p>Aanvraagmethode ( <span class="codeph"> GET </span>, <span class="codeph"> POST </span> enzovoort). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %O  </span> </p> </td> 
   <td> <p>Verzoek om overlapping (aantal verzoeken die gelijktijdig worden verwerkt). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %p  </span> </p> </td> 
   <td> <p>Lokale poort waarop dit verzoek is ontvangen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %q  </span> </p> </td> 
   <td> <p>De koord van de vraag (voorvoegd met "?" indien aanwezig). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %r  </span> </p> </td> 
   <td> <p>Eerste regel van request (aanvraagmethode, URI, HTTP-versie). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %R  </span> </p> </td> 
   <td> <p>Hetzelfde als <span class="codeph"> %r </span>, maar past beperkte HTTP-codering toe op de URI om problemen met logparsering te voorkomen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %s  </span> </p> </td> 
   <td> <p>HTTP response status code. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %S  </span> </p> </td> 
   <td> <p>Gebruiker sessie-id. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %t  </span> </p> </td> 
   <td> <p>Datum en tijd, in de indeling Common Log. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %u  </span> </p> </td> 
   <td> <p>Externe gebruiker die is geverifieerd (indien aanwezig), anders ''. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %U  </span> </p> </td> 
   <td> <p>URI-pad. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %v  </span> </p> </td> 
   <td> <p>Lokale servernaam. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %T  </span> </p> </td> 
   <td> <p>Verwerkingsduur aanvragen in seconden. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheKey}r  </span> </p> </td> 
   <td> <p>Cachetoets Platform Server (cachebestandsmap/naam). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheUse}r  </span> </p> </td> 
   <td> <p>Platform Server cache management keyword: <span class="codeph"> { REUSED | GECREËERD | BIJGEWERKT | EXTERN | REMOTE_CREATED | REMOTE_UPDATED | REMOTE_CACHE | GEVALIDEERD | GENEGEERD | ONGEDEFINIEERD } </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ContentType}r  </span> </p> </td> 
   <td> <p>Het MIME-type voor reactie. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>%{Context}r </p> </td> 
   <td> <p>De doelcontext als een context door:sturen voorkomt. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Digest}r  </span> </p> </td> 
   <td> <p>De <span class="codeph">-waarde voor de responsheader </span> (MD5-handtekening van de reactiegegevens). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Exception}r  </span> </p> </td> 
   <td> <p>Foutbericht. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{FetchTime}r  </span> </p> </td> 
   <td> <p>De tijd die wordt genomen om geheim voorgeheugeningang of gegevens van de Server van het Beeld terug te winnen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ParseTime}r  </span> </p> </td> 
   <td> <p>Tijd die nodig is voor het parseren van aanvragen en het opzoeken van de afbeeldingscatalogus. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PathBasedAccess}r  </span> </p> </td> 
   <td> <p>Geeft aan of met deze aanvraag al dan niet werd geprobeerd padgebaseerde toegang te verkrijgen buiten het catalogussysteem. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PeerServer}r  </span> </p> </td> 
   <td> <p>IP adres van de peer server in de geheim voorgeheugencluster die de geheim voorgeheugeningang of "-"leverde als <span class="codeph"> CacheUse </span> noch <span class="codeph"> REMOTE_CREATED </span> noch <span class="codeph"> REMOTE_UPDATED </span> is. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ProcessingStatus}r  </span> </p> </td> 
   <td> <p>Foutcategorie: </p> <p> 
     <ul id="ul_BA2A18337D374939AC9BF2424247E40F"> 
      <li id="li_0A2410F03E1A41078F8E8FDF34531810"> <p>0=geen fout. </p> </li> 
      <li id="li_CCEE27F75BD34195895428188B2C30AA"> <p>1=afbeelding(en) niet gevonden op de server. </p> </li> 
      <li id="li_315BBCC7B4C1443495C9C2B3F9800C1F"> <p> 2=IS-protocolgebruiksfout of een andere inhoudsfout dan 1. </p> </li> 
      <li id="li_E028FFF165BD4535875F8684FCAF1859"> <p>3=andere serverfout. </p> </li> 
      <li id="li_5AFFB0EE80484885BCDACD9DF3EF58F7"> <p>4=request geweigerd vanwege tijdelijke overbelasting van de server. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ReqType}r  </span> </p> </td> 
   <td> <p>De naar boven georiënteerde waarde van <span class="codeph"> req= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{RootId}r  </span> </p> </td> 
   <td> <p>De basis-id van de hoofdcatalogus van de aanvraag. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{SendTime}r  </span> </p> </td> 
   <td> <p>De tijd het de Server van het Platform neemt om reactie te verzenden na het schrijven van gegevens aan de outputstroom. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Size}r  </span> </p> </td> 
   <td> <p>Als <span class="codeph"> %B </span>, maar omvat waarden voor (niet gewijzigde) reacties 304. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{TransformedUrl}r  </span> </p> </td> 
   <td> <p>De laatste URL na alle transformaties van de liniaal. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{  <span class="varname"> httpRequestHeader  </span>}i  </span> </p> </td> 
   <td> <p>De waarde van de opgegeven HTTP-aanvraagheader. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{  <span class="varname"> httpResponseHeader  </span>}  </span> </p> </td> 
   <td> <p>De waarde van de opgegeven HTTP-responsheader. </p> </td> 
  </tr> 
 </tbody> 
</table>

Standaard is `"%G %a %s %{ProcessingStatus}r %{Size}r %D %{ParseTime}r %{FetchTime}r %O %{ReqType}r '%{RootId}r' %{CacheUse}r %R [%I] '%{Referer}i' %{Host}i %{X-Forwarded-For}i %{If-None-Match}i %{If-Match}i %{If-Modified-Since}i %{Digest}r %{ContentType}r %p %{Exception}r %{CacheKey}r %{PeerServer}" %{SendTime}r %{Context}r %{TransformedUrl}r %{PathBasedAccess}r.`
