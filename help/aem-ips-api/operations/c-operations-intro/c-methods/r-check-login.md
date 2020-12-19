---
description: Controleert of een gebruiker met een specifiek bedrijf (geïdentificeerd door greep), e-mailadres, en wachtwoord zich kan aanmelden.
seo-description: Controleert of een gebruiker met een specifiek bedrijf (geïdentificeerd door greep), e-mailadres, en wachtwoord zich kan aanmelden.
seo-title: checkLogin
solution: Experience Manager
title: checkLogin
topic: Scene7 Image Production System API
uuid: 69f9e5f6-50c2-403d-93b2-b84a01f512a9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---


# checkLogin{#checklogin}

Controleert of een gebruiker met een specifiek bedrijf (geïdentificeerd door greep), e-mailadres, en wachtwoord zich kan aanmelden.

>[!NOTE]
>
>Als het bedrijfshandvat wordt weggelaten, controleert deze methode login van de standaardgebruiker.

## Toegestane gebruikerstypen {#section-df8b26b550854f899948276adaca083a}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-1ad4c0b4803b4388aedd655030676cb3}

**Invoer (checkLoginParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Nee | De handgreep aan het bedrijf dat de gebruiker bevat. |
| ` *`email`*` | `xsd:string` | Ja | Het e-mailadres van de gebruiker. |
| ` *`password`*` | `xsd:string` | Ja | Het wachtwoord van de gebruiker. |

**Uitvoer (checkLoginParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`status`*` | `xsd:string` | Ja | Aanmeldingsstatus van gebruiker. |

## Voorbeelden {#section-23f90100a9d94bc7b4045634cccd1b98}

Deze steekproefcode gebruikt een parameter van het bedrijfshandvat, e-mailadres, en een wachtwoord om te bepalen als een gebruiker aan IPS kan login. Als de gebruiker *can* login, deze methode het koord, `ValidLogin` terugkeert. Als de gebruiker *niet* login kan, keert deze methode het koord, `InvalidLogin` terug.

**Verzoek**

```java
<ns1:checkLoginParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>137</ns1:companyHandle>
   <ns1:email>juser3@scene7.com</ns1:email>
   <ns1:password>welcome</ns1:password>
</ns1:checkLoginParam>
```

**Antwoord**

```java
<ns1:checkLoginReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:status>InvalidLogin</ns1:status>
</ns1:checkLoginReturn>
```

