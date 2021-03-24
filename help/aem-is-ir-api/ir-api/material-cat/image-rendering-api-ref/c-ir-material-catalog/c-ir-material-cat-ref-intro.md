---
description: In dit document wordt de materiaalcatalogus voor Dynamic Media Image Rendering beschreven.
solution: Experience Manager
title: Inleiding
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---


# Inleiding{#introduction}

In dit document wordt de materiaalcatalogus voor Dynamic Media Image Rendering beschreven.

**Beoogd publiek**

Deze documentatie is bedoeld voor ervaren programmeurs en ontwikkelaars van websites die Dynamic Media Image Rendering willen gebruiken voor een website of een aangepaste toepassing.

Aangenomen wordt dat de lezer bekend is met Dynamic Media Image Authoring and Image Rendering, algemene HTTP-protocolstandaarden en -conventies en basisterminologie voor beeldbewerking.

**Documentconventies**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Letterlijk </p> </td> 
  <td class="stentry"> <p>In syntaxissecties is niet-cursieve tekst letterlijk; dit geldt niet voor witruimte en de symbolen [ ] { } | *. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'letterlijk' </p> </td> 
  <td class="stentry"> <p>In beschrijvende gedeelten is niet-cursieve tekst tussen enkele aanhalingstekens letterlijk. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> parameter  </span> </p> </td> 
  <td class="stentry"> <p>Cursief verwijst naar een variabele of parameter, die moet worden vervangen door een werkelijke waarde. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> attribute::Item  </span> </p> </td> 
  <td class="stentry"> <p>Een naam met het voorvoegsel 'attribute::' verwijst naar een afbeeldingscataloguskenmerk. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="codeph"> catalogus::Item  </span> </td> 
  <td class="stentry"> <p>Een naam vooraf voorzien van 'catalog::' verwijst naar een gegevensveld voor een materiaalcatalogus. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::Item  </span> </p> </td> 
  <td class="stentry"> <p>Een naam met de voorvoegsel 'icc::' verwijst naar een veld in de ICC-kleurenprofielkaart. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> macro::Item  </span> </p> </td> 
  <td class="stentry"> <p>Een naam met het voorvoegsel 'macro::' verwijst naar een veld in de macrodefinitietabel. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> regels:Item  </span> </p> </td> 
  <td class="stentry"> <p>Een naam met een voorvoegsel 'ruleset::' verwijst naar een element in een URL-voorverwerkingsregelset. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> default::Item  </span> </p> </td> 
  <td class="stentry"> <p>Een naam met de voorvoegsel 'default:' verwijst naar een kenmerk van de standaardafbeeldingscatalogus. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> vignet::Item  </span> </p> </td> 
  <td class="stentry"> <p>Een naam met de voorvoegsel 'vignet::' verwijst naar een veld in de vignetkaart. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>[ <span class="varname"> optioneel </span> ] </p> </td> 
  <td class="stentry"> <p>Optionele syntaxiselementen staan tussen vierkante haakjes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*[ <span class="varname"> optioneel </span> ] </p> </td> 
  <td class="stentry"> <p>Het optionele syntaxiselement mag nooit of vaker worden herhaald. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> item1  </span>|  <span class="varname"> post 2  </span> </p> </td> 
  <td class="stentry"> <p>Een verticale balk geeft aan dat het enige syntaxisitem links of het item rechts kan worden gebruikt. Er moet precies één item zijn geselecteerd. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>{ <span class="varname"> groep </span> } </p> </td> 
  <td class="stentry"> <p>accolades worden gebruikt om syntaxiselementen te groeperen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*{ <span class="varname"> groep </span> } </p> </td> 
  <td class="stentry"> <p>De syntaxiselementen in de groep kunnen een of meer keren worden herhaald. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Witruimte. </p> </td> 
  <td class="stentry"> <p>Spaties (spaties of tabs) zijn niet toegestaan in HTTP-aanvragen. Dit document gebruikt soms alleen voor de duidelijkheid witruimte tussen syntactische elementen. </p> </td> 
 </tr> 
</table>

