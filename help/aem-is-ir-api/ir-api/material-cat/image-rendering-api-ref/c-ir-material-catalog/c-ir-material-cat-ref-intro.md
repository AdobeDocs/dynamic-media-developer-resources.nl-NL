---
description: Dit document beschrijft de materiaalcatalogus voor Scene7 het Teruggeven van het Beeld.
seo-description: Dit document beschrijft de materiaalcatalogus voor Scene7 het Teruggeven van het Beeld.
seo-title: Inleiding
solution: Experience Manager
title: Inleiding
topic: Scene7 Image Serving - Image Rendering API
uuid: 38da0561-7730-4170-bf29-02de325b3ad9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Inleiding{#introduction}

Dit document beschrijft de materiaalcatalogus voor Scene7 het Teruggeven van het Beeld.

**Beoogd publiek**

Dit gedocumenteerd is bedoeld voor ervaren programmeurs en websiteontwikkelaars die Scene7 het Teruggeven van het Beeld voor een website of een douanetoepassing willen gebruiken.

Men veronderstelt dat de lezer met het Authoring en het Teruggeven van het Beeld Scene7, algemene het protocolnormen en de overeenkomsten van HTTP, en basisimaging terminologie vertrouwd is.

**Documentconventies**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Letterlijk </p> </td> 
  <td class="stentry"> <p>In syntaxissecties is niet-cursieve tekst letterlijk; dit geldt niet voor witruimte en de symbolen [ ] { }| *. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'letterlijk' </p> </td> 
  <td class="stentry"> <p>In beschrijvende gedeelten is niet-cursieve tekst tussen enkele aanhalingstekens letterlijk. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> parameter </span> </p> </td> 
  <td class="stentry"> <p>Cursief verwijst naar een variabele of parameter, die moet worden vervangen door een werkelijke waarde. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> attribute::Item </span> </p> </td> 
  <td class="stentry"> <p>Een naam met het voorvoegsel 'attribute::' verwijst naar een afbeeldingscataloguskenmerk. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="codeph"> catalogus::Item </span> </td> 
  <td class="stentry"> <p>Een naam vooraf voorzien van 'catalog::' verwijst naar een gegevensveld voor een materiaalcatalogus. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::Item </span> </p> </td> 
  <td class="stentry"> <p>Een naam met de voorvoegsel 'icc::' verwijst naar een veld in de ICC-kleurenprofielkaart. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> macro::Item </span> </p> </td> 
  <td class="stentry"> <p>Een naam met het voorvoegsel 'macro::' verwijst naar een veld in de macrodefinitietabel. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> regels:Item </span> </p> </td> 
  <td class="stentry"> <p>Een naam met een voorvoegsel 'ruleset::' verwijst naar een element in een URL-voorverwerkingsregelset. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> default::Item </span> </p> </td> 
  <td class="stentry"> <p>Een naam met de voorvoegsel 'default:' verwijst naar een kenmerk van de standaardafbeeldingscatalogus. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> vignet::Item </span> </p> </td> 
  <td class="stentry"> <p>Een naam met de voorvoegsel 'vignet::' verwijst naar een veld in de vignetkaart. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>[ <span class="varname"> optional </span> ] </p> </td> 
  <td class="stentry"> <p>Optionele syntaxiselementen staan tussen vierkante haakjes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*[ <span class="varname"> optional </span> ] </p> </td> 
  <td class="stentry"> <p>Het optionele syntaxiselement mag nooit of vaker worden herhaald. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> item1 </span>| <span class="varname"> post 2 </span> </p> </td> 
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

