---
description: Hiermee genereert u een nieuw wachtwoord.
solution: Experience Manager
title: generatePassword
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 80e7642f-4aec-4ff0-a090-e59b7a065c39
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 0%

---

# generatePassword{#generatepassword}

Hiermee genereert u een nieuw wachtwoord.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-88f7dc11e5c74be281399d8f2e3c9555}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-d516615c906240819a284786efb19863}

**Input (generatePasswordParam)**

Geen.

**Output (generatePasswordParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| password | `xsd:string` | Ja | Een nieuw wachtwoord. |

## Voorbeelden {#section-f580fefdccec46fe95359e3aef0ed17f}

In dit codevoorbeeld wordt een wachtwoord gegenereerd. Dit is ongebruikelijk omdat de aanvraag gewoon een parameter is zonder ingesloten elementen of waarden. IPS keert een sterk wachtwoord terug.

**Verzoek**

```java
<generatePasswordParam xmlns="http://www.scene7.com/IpsApi/xsd">
</generatePasswordParam>
```

**Antwoord**

```java
<generatePasswordReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <password>1\7aQRn]</password>
</generatePasswordReturn>
```
