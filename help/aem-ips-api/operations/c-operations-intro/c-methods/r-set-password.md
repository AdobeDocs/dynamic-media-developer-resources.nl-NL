---
description: Hiermee stelt u het wachtwoord van een specifieke gebruiker of de standaardgebruiker in op een specifieke waarde, afhankelijk van het feit of u een gebruikershandgreep opgeeft.
seo-description: Hiermee stelt u het wachtwoord van een specifieke gebruiker of de standaardgebruiker in op een specifieke waarde, afhankelijk van het feit of u een gebruikershandgreep opgeeft.
seo-title: setPassword
solution: Experience Manager
title: setPassword
topic: Scene7 Image Production System API
uuid: 78067f8d-4191-4580-a5a8-adb6edfcfab8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setPassword{#setpassword}

Hiermee stelt u het wachtwoord van een specifieke gebruiker of de standaardgebruiker in op een specifieke waarde, afhankelijk van het feit of u een gebruikershandgreep opgeeft.

Vervaldatum wachtwoord is optioneel. Als u dit weglaat, verloopt het wachtwoord nooit.

## Typen geautoriseerde gebruikers {#section-39ae61d78cab4492a6efc1fc0d2f06c4}

>[!NOTE]
>
>*Slechts* wordt het `IpsAdmin` gebruikerstype geautoriseerd om reeksPassword vraag tegen andere gebruikers in werking te stellen.

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`

## Parameters {#section-0531294341f7483d89dacaa393dd659a}

**Input (setPasswordParam)**

<table id="table_BF54512811344E0B979C5070354E8048"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Naam </p> </th> 
   <th colname="col2" class="entry"> <p>Type </p> </th> 
   <th colname="col3" class="entry"> <p>Vereist </p> </th> 
   <th colname="col4" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> gebruikershandgreep </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:tekenreeks </span> </p> </td> 
   <td colname="col3"> <p>Nee </p> </td> 
   <td colname="col4"> <p>Gebruikershandgreep. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> wachtwoord </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:tekenreeks </span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Wachtwoord. </p> <p>De volgende vereisten worden afgedwongen op het gekozen wachtwoord: </p> <p> 
     <ul id="ul_E5BE3621127C476788412174584075B3"> 
      <li id="li_0132852AFD774659A0224C450F19418C">Wachtwoorden zijn hoofdlettergevoelig. </li> 
      <li id="li_71224B3A89C8461AB689BAD383EC8CEA">De minimale lengte van wachtwoorden is acht tekens. </li> 
      <li id="li_C21B6843EA734D1ABE0580185F775408">Het wachtwoord moet een of meer tekens van de volgende tekenklassen bevatten: 
       <ul id="ul_D5D3911AD6214035BBD2AB8350A459C7"> 
        <li id="li_6E3F084100104F2CBCF130EF8852C7B7">Engelse kleine letters. Bijvoorbeeld <span class="codeph"> b c d e </span> enzovoort </li> 
        <li id="li_1FDED8D7348842BC857320D797D41217">Engelse tekens in hoofdletters. Bijvoorbeeld, <span class="codeph"> A B C D E </span> enzovoort. </li> 
        <li id="li_C3C4D5412AA749F3B78F37B2B696CF80">Getallen. Bijvoorbeeld <span class="codeph"> 1 2 3 4 5 </span> enzovoort. </li> 
        <li id="li_2730798F26E74B878BEDE510CD06D8DD">Speciale symbooltekens. U kunt bijvoorbeeld een van de volgende handelingen uitvoeren: <span class="codeph"> ` ~ ! @ # $ % ^ * ( ) _ + - = { }| [ ] &amp; \ : " ; ' &lt; &gt; ? , . / </span> </li> 
       </ul> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> passwordExpiers </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:dateTime </span> </p> </td> 
   <td colname="col3"> <p>Nee </p> </td> 
   <td colname="col4"> <p>Bepaalt de vervaldatum van het wachtwoord. <p>Opmerking:  Geef de tijdzone het verzoek voor dit veld. Tijdzones worden aangepast aan de Central Time. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (setPasswordReturn)**

IPS API keert geen reactie voor deze verrichting terug.

## Voorbeelden {#section-23a6fbabdb3c4c3180076057e47ae567}

In dit codevoorbeeld wordt een gebruikerswachtwoord gemaakt. Het wachtwoord verloopt nooit omdat `passwordExpires` het is weggelaten.

**Verzoek**

```java
<ns1:setPasswordParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">  
   <ns1:userHandle>3341|juser@scene7.com</ns1:userHandle> 
   <ns1:password>@Do6e$ySt3mz</ns1:password> 
</ns1:setPasswordParam>
```

**Antwoord**

Geen.
