---
description: Bedrijfsspecifieke configuratie-instellingen.
seo-description: Bedrijfsspecifieke configuratie-instellingen.
seo-title: CompanySettings
solution: Experience Manager
title: CompanySettings
topic: Scene7 Image Production System API
uuid: a807d5c1-058d-4313-b4f8-6ee203284003
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# CompanySettings{#companysettings}

Bedrijfsspecifieke configuratie-instellingen.

Syntaxis

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Naam | Type | Beschrijving |
|---|---|---|
| ` *`overwriteMode`*` | `xsd:string` | Hiermee wordt bepaald of afbeeldingen in de huidige map met dezelfde basisafbeeldingsnaam en extensie moeten worden overschreven. |
| ` *`preservePublishState`*` | `xsd:boolean` | Geeft aan of een vervangende afbeelding die in IPS is geüpload de bestaande instelling &quot;Klaar voor publicatie&quot; moet behouden of dat deze moet worden zoals opgegeven door het uploaden. |
| ` *`defaultSourceProfile`*` | `types:Asset` | Hiermee wordt het standaardbronkleurprofiel (Coated FOGRA27 (ISO 126472:2004)) opgegeven dat automatisch wordt toegepast als onderdeel van het standaardkleurgedrag gebruiken bij het toevoegen van CMYK-afbeeldingsbestanden. |
| ` *`defaultDisplayProfile`*` | `types:Asset` | Hiermee wordt het standaard interne kleurprofiel (U.S. Web Coated (SWOP) v2) opgegeven dat automatisch wordt toegepast als onderdeel van het standaardkleurgedrag gebruiken bij het toevoegen van CMYK-afbeeldingsbestanden. |
| ` *`iptcExifMappingXslt`*` | `types:Asset` | De extractie van IPTC- en EXIF-afbeeldingskoptekstgegevens naar IPS vereist een conversie van interne veldnamen naar door de gebruiker gedefinieerde veldnamen voor het bedrijf. Hiermee wordt een XSL-vertaaltabel bepaald (de standaardinstelling is Geen IPTC- of EXIF-velden extraheren) voor geüploade afbeeldingen. |
| ` *`xmpMappingXslt`*` | `types:Asset` | Voor het extraheren van XMP-afbeeldingskoptekstgegevens naar IPS is een omzetting van interne veldnamen naar door de gebruiker gedefinieerde veldnamen voor het bedrijf vereist. Hiermee wordt een XSL-vertaaltabel bepaald (standaard is &quot;Geen XMP-velden extraheren&quot;) voor geüploade afbeeldingen. |
| ` *`diskSpaceWarningMin`*` | `xsd:int` | Minimale hoeveelheid schijfruimte voor afbeeldingsdirectory voordat een waarschuwing wordt verzonden. |
| ` *`emailTrashCleanupWarning`*` | `xsd:boolean` | Hiermee bepaalt u of e-mailberichten worden verzonden voordat objecten die in de prullenbak zijn geplaatst, automatisch worden verwijderd. |
| ` *`javascriptUploadEnabled`*` | `types:Asset` | Hiermee wordt bepaald of JavaScript-bestanden moeten worden geüpload. Dit is een potentieel veiligheidsrisico, dus gebruik deze optie met zorg. |

