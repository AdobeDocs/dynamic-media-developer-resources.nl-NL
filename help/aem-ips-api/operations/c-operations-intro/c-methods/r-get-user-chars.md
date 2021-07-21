---
description: Hiermee wordt een lijst opgehaald met de tekens die in een bepaald veld worden gebruikt.
solution: Experience Manager
title: getUserChars
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: d6b79c06-0e90-406f-bac8-3b8c2bae5480
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# getUserChars{#getuserchars}

Hiermee wordt een lijst opgehaald met de tekens die in een bepaald veld worden gebruikt.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-7023871be4d2442daf51ff060ca06d9a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameters {#section-93107d87f1b24fc8ad276dfee5e30b63}

**Input (getUserCharsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`charField`*` | `xsd:string` | Ja | Hiermee bepaalt u de status van de prullenbak waarnaar u wilt zoeken. |
| `*`includeInactive`*` | `xsd:boolean` | Ja | Inactieve gebruikers opnemen of uitsluiten. De niet-IPS gebruikers Admin moeten een actief lid van minstens één bedrijf zijn om worden gemachtigd om het even welke API vraag te maken. Een vergunningsfout zal zijn teruggekeerd als de gebruiker geen actief bedrijflidmaatschap heeft. |
| `*`includeInvalid`*` | `xsd:boolean` | Nee | Ongeldige gebruikers opnemen of uitsluiten. |
| `*`companyHandleArray`*` | `types:HandleArray` | Nee | De resultaten van de filter die op bedrijf worden gebaseerd. |
| `*`groupHandleArray`*` | `types:HandleArray` | Nee | Hiermee filtert u resultaten op basis van groepen. |
| `*`userRoleArray`*` | `types:StringArray` | Nee | Hiermee filtert u resultaten op basis van gebruikersrol. |
| `*`numChars`*` | `xsd:int` | Nee | >1 teken inschakelen. |

**Output (getUserCharsReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`userCharsArray`*` | `types:StringArray` | Ja | Een array met tekenvoorvoegsels. |

## Voorbeelden {#section-3702f165e8b041139a6144f4a76ca25f}

Dit codevoorbeeld retourneert:

* Eerste tekens van de achternaam van de gebruikers van een bepaald bedrijf.
* Een set groepen.
* Een set gebruikersrollen.

De tekenreeksconstante van de Filtervelden Gebruikersteken bepaalt het type van de geretourneerde gebruikerstekens.

**Verzoek**

```java
<ns1:getUserCharsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:charField>LastName</ns1:charField>
   <ns1:includeInvalid>false</ns1:includeInvalid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:getUserCharsParam>
```

**Antwoord**

```java
<getUserCharsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userCharsArray>
      <items>b</items>
      <items>c</items>
      <items>d</items>
   </userCharsArray>
</getUserCharsReturn>
```
