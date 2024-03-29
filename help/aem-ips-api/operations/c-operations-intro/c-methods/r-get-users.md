---
description: Hiermee wordt een array met gebruikers opgehaald, zoals is opgegeven door het bedrijf, de groep en de handgrepen voor de gebruikersrol. Met deze bewerking kunt u geretourneerde gebruikers sorteren en filteren op teken.
solution: Experience Manager
title: getUsers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dfdcbcdd-232f-4c73-9520-c7c958eedf54
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# getUsers{#getusers}

Hiermee wordt een array met gebruikers opgehaald, zoals is opgegeven door het bedrijf, de groep en de handgrepen voor de gebruikersrol. Met deze bewerking kunt u geretourneerde gebruikers sorteren en filteren op teken.

## Geautoriseerde gebruikerstypen {#section-6a8f23cc6b22442d8776f701016971ed}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`


| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| includeInactive | `xsd:boolean` | Nee | Inactieve gebruikers opnemen of uitsluiten. De niet-IPS gebruikers Admin moeten een actief lid van minstens één bedrijf zijn om worden gemachtigd om het even welke API vraag te maken. Een vergunningsfout is teruggekeerd als de gebruiker geen actief bedrijflidmaatschap heeft. |
| includeInvalid | `xsd:boolean` | Nee | Hiermee kunt u ongeldige gebruikers opnemen in- of uitsluiten. |
| companyHandleArray | `types:HandleArray` | Nee | Filterresultaten per bedrijf. |
| groupHandleArray | `types:HandleArray` | Nee | Filterresultaten per groep. |
| userRoleArray | `types:StringArray` | Nee | De resultaten van de filter door gebruikersrol. |
| charFilterField | `xsd:string` | Nee | Filterresultaten op tekenreeksvoorvoegsel van veld (zie [!DNL Trash State).] |
| charFilter | `xsd:string` | Nee | Filterresultaten met een specifiek teken. |
| sortBy | `xsd:string` | Nee | Keuze van sorteervelden voor gebruikers. |
| recordsPerPage | `xsd:int` | Nee | Retourneert het opgegeven aantal records per pagina. |
| resultsPage | `xsd:int` | Nee | Resultaatpagina. |

**Output (getUsersReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| userArray | `types:UserArray` | Ja | Een array met gebruikers. |

## Voorbeelden {#section-bc43a5dd7b4c4f048d25fc881554dab2}

Deze codesteekproef keert de serie van gebruikers voor verscheidene facultatieve parameters terug. Gebruikersrollen, filtervelden voor gebruikerstekens en sorteervelden worden bepaald met behulp van specifieke tekenreeksconstanten.

**Verzoek**

```java
<ns1:getUsersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:includeInvalid>false</ns1:includeInvalid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
   <ns1:userRoleArray>
      <ns1:items>IpsAdmin</ns1:items>
   </ns1:userRoleArray>
   <ns1:sortBy>LastName</ns1:sortBy>
</ns1:getUsersParam>
```

**Antwoord**

```java
<getUsersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userArray>
      <items>
         <userHandle>70|kmagnusson@adobe.com</userHandle>
         <firstName>Kris</firstName>
         <lastName>Magnusson</lastName>
         <email>kmagnusson@adobe.com</email>
         <role>IpsAdmin</role>
         <isValid>true</isValid>
         <passwordExpires>2107-07-27T15:18:15.816-07:00</passwordExpires>
      </items>
      ...
   </userArray>
</getUsersReturn>
```
