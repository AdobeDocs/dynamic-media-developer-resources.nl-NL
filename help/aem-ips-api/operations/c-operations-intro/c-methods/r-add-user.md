---
description: Maakt een gebruikersaccount en voegt die account toe aan een of meer bedrijven.
solution: Experience Manager
title: addUser
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: aed39e73-f528-4c26-8f62-c3d796e9101a
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---

# addUser{#adduser}

Maakt een gebruikersaccount en voegt die account toe aan een of meer bedrijven.

Wanneer het toevoegen van een gebruiker aan veelvoudige bedrijven, specificeer die bedrijven door hun bedrijfshandvatten binnen `companyHandleArray`. Deze bewerking retourneert de greep naar de gebruiker die u zojuist hebt toegevoegd.

## Geautoriseerde gebruikerstypen {#section-126ad42f844444fea11ecf8ad01fe1ec}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameters {#section-40390a512e314b8d80ecffbb7729f6fb}

**Input (addUserParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| firstName | `xsd:string` | Ja | De voornaam van de gebruiker. |
| lastName | `xsd:string` | Ja | De achternaam van de gebruiker. |
| email | `xsd:string` | Ja | Het e-mailadres van de gebruiker. |
| defaultRole | `xsd:string` | Ja | Plaatst de rol voor een gebruiker in elk bedrijf zij tot behoren. De `IpsAdmin` de rol treedt andere per-bedrijfmontages met voeten. |
| password | `xsd:string` | Ja | Hiermee wordt het wachtwoord van de gebruiker ingesteld |
| passwordExpires | `xsd:dateTime` | Nee | Hiermee stelt u de verloopperiode voor het wachtwoord in. Geef de tijdzone op wanneer u het verzoek doorgeeft. Tijdzones worden aangepast aan de Central Time. |
| isValid | `xsd:boolean` | Ja | Hiermee wordt bepaald of de gebruiker geldig is. |
| membershipArray | `xsd:CompanyMembershipUpdateArray` | Ja | Een array met bedrijfshandgrepen. |

**Output (addUserParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| userHandle | `xsd:string` | Ja | De greep voor de gebruiker. |

## Voorbeelden {#section-2547cef622734b71919eef849960b5cb}

De IPS API keert een gebruikershandvatelement terug dat de nieuwe gebruiker specificeert.

**Verzoek**

```java {.line-numbers}
<ns1:addUserParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:firstName>Joe</ns1:firstName>
   <ns1:lastName>User</ns1:lastName>
   <ns1:email>juser@adobe.com</ns1:email>
   <ns1:defaultRole>TrialSiteUser</ns1:role>
   <ns1:password>passw0rd</ns1:password>
   <ns1:isValid>true</ns1:isValid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:addUserParam>
```

**Antwoord**

```java {.line-numbers}
<ns1:addUserReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>525s|juser@scene7.com</ns1:userHandle>
</ns1:addUserReturn>
```
