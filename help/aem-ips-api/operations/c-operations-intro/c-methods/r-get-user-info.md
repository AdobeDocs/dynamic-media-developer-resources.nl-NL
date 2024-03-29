---
description: Hiermee wordt informatie over een gebruiker opgehaald. Gebruik het e-mailadres en het wachtwoord van een systeemgebruiker als referenties voor het autoriseren van de aanvraag. Anders krijgt de bewerking informatie over de standaardgebruiker.
solution: Experience Manager
title: getUserInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1981f25f-779e-4434-ab6b-0debb40521fe
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---

# getUserInfo{#getuserinfo}

Hiermee wordt informatie over een gebruiker opgehaald. Gebruik het e-mailadres en het wachtwoord van een systeemgebruiker als referenties voor het autoriseren van de aanvraag. Anders krijgt de bewerking informatie over de standaardgebruiker.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-1c42d78e914a4b84a946b3480f29b36a}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-e87b3cb743494719925c9458eed433b6}

**Input (getUserInfoParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| userHandle | `xsd:string` | Nee | Verwerk de gebruiker van wie u de gegevens wilt retourneren. |
| email | `xsd:string` | Nee | E-mailadres van gebruiker. |

**Output (getUserInfoReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| userInfo | `types:User` | Ja | De voornaam, achternaam, het e-mailadres en de rol van een gebruiker, evenals of de gebruiker geldig is en wanneer het wachtwoord van de gebruiker verloopt. |

## Voorbeelden {#section-98d77a2e360a438dbe240099bea26a65}

Deze codesteekproef keert informatie voor de standaardIPS gebruiker terug.

**Verzoek**

```java
<getUserInfoParam xmlns="http://www.scene7.com/IpsApi/xsd" /></getUserInfoParam>
```

**Antwoord**

```java
<ns1:getUserInfoReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd"> 
   <ns1:userInfo> 
      <ns1:userHandle>3261|user@scene7.com</ns1:userHandle> 
      <ns1:firstName>FirstName</ns1:firstName> 
      <ns1:lastName>LastName</ns1:lastName> 
      <ns1:email>user@scene7.com</ns1:email> 
      <ns1:role>IpsAdmin</ns1:role> 
      <ns1:isValid>true</ns1:isValid> 
      <ns1:passwordExpires>2107-04-22T18:35:41.995Z</ns1:passwordExpires> 
   </ns1:userInfo> 
</ns1:getUserInfoReturn>
```
