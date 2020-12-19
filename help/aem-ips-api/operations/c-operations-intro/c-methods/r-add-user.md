---
description: Maakt een gebruikersaccount en voegt die account toe aan een of meer bedrijven.
seo-description: Maakt een gebruikersaccount en voegt die account toe aan een of meer bedrijven.
seo-title: addUser
solution: Experience Manager
title: addUser
topic: Scene7 Image Production System API
uuid: b8c5ada6-470e-4795-a4f3-20750da709a9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---


# addUser{#adduser}

Maakt een gebruikersaccount en voegt die account toe aan een of meer bedrijven.

Wanneer het toevoegen van een gebruiker aan veelvoudige bedrijven, specificeer die bedrijven door hun bedrijfshandvatten in `companyHandleArray`. Deze bewerking retourneert de greep naar de gebruiker die u zojuist hebt toegevoegd.

## Toegestane gebruikerstypen {#section-126ad42f844444fea11ecf8ad01fe1ec}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameters {#section-40390a512e314b8d80ecffbb7729f6fb}

**Input (addUserParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`firstName`*` | `xsd:string` | Ja | De voornaam van de gebruiker. |
| ` *`lastName`*` | `xsd:string` | Ja | De achternaam van de gebruiker. |
| ` *`email`*` | `xsd:string` | Ja | Het e-mailadres van de gebruiker. |
| ` *`defaultRole`*` | `xsd:string` | Ja | Plaatst de rol voor een gebruiker in elk bedrijf zij tot behoren. De rol `IpsAdmin` negeert echter andere instellingen per bedrijf. |
| ` *`password`*` | `xsd:string` | Ja | Hiermee wordt het wachtwoord van de gebruiker ingesteld |
| ` *`passwordExpires`*` | `xsd:dateTime` | Nee | Hiermee stelt u de verloopperiode voor het wachtwoord in. Geef de tijdzone op wanneer u het verzoek doorgeeft. Tijdzones worden aangepast aan de Central Time. |
| ` *`isValid`*` | `xsd:boolean` | Ja | Hiermee wordt bepaald of de gebruiker geldig is. |
| ` *`membershipArray`*` | `xsd:CompanyMembershipUpdateArray` | Ja | Een array met bedrijfshandgrepen. |

**Output (addUserParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`userHandle`*` | `xsd:string` | Ja | De greep voor de gebruiker. |

## Voorbeelden {#section-2547cef622734b71919eef849960b5cb}

De IPS API keert een gebruikershandvatelement terug dat de nieuwe gebruiker specificeert.

**Verzoek**

```java
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

```java
<ns1:addUserReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>525s|juser@scene7.com</ns1:userHandle>
</ns1:addUserReturn>
```

