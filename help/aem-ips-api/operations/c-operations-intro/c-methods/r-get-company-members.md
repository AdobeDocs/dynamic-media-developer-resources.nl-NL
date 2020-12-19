---
description: Retourneert de gebruikers van een bedrijf dat is opgegeven door een greep van het bedrijf.
seo-description: Retourneert de gebruikers van een bedrijf dat is opgegeven door een greep van het bedrijf.
seo-title: getCompanyMember
solution: Experience Manager
title: getCompanyMember
topic: Scene7 Image Production System API
uuid: 45e2d040-a70a-46f4-863a-633ddabcbcf6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---


# getCompanymembers{#getcompanymembers}

Retourneert de gebruikers van een bedrijf dat is opgegeven door een greep van het bedrijf.

Syntaxis

## Toegestane gebruikerstypen {#section-b2bc2fa0cc944cea8be82524838307cc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameters {#section-5602e4d6f2214e398e6a804e61f1a088}

**Input (getCompanyMemberParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | De handgreep aan het bedrijf waarvan leden u wilt verkrijgen. |
| ` *`includeInvalid`*` | `xsd:boolean` | Ja | Inclusief ongeldige bedrijven. |

**Output (getCompanyMemberReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`memberArray`*` | `types:CompanyMemberArray` | Ja | Array met gebruikerslidmaatschappen. |

## Voorbeelden {#section-39d8cf3653fd4fe8b842caabac9dedfc}

Deze codesteekproef keert alle leden van een bedrijf in een gebruikersserie terug. De reactie is afgebroken voor de beknoptheid.

**Verzoek**

```java
<ns1:getCompanyMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:includeInvalid>false</ns1:includeInvalid>
</ns1:getCompanyMembersParam>
```

**Antwoord**

```java
<getCompanyMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <memberArray>
      <items>
         <userHandle>66|pbayol@adobe.com</userHandle>
         <firstName>Peter</firstName>
         <lastName>Bayol</lastName>
         <email>pbayol@adobe.com</email>
         <role>IpsAdmin</role>
         <isValid>true</isValid>
         <passwordExpires>2107-07-25T23:12:49.472-07:00</passwordExpires>
      </items>
      ...
   </memberArray>
</getCompanyMembersReturn>
```

