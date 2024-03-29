---
description: Bedrijfsspecifieke configuratie-instellingen.
solution: Experience Manager
title: CompanySettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82e6362d-beab-47ff-bb20-11047f0d8787
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---

# [!DNL CompanySettings]{#companysettings}

Bedrijfsspecifieke configuratie-instellingen.

Syntaxis

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Naam | Type | Beschrijving |
|---|---|---|
| overwriteMode | `xsd:string` | Hiermee wordt bepaald of afbeeldingen in de huidige map moeten worden overschreven met dezelfde naam en extensie voor de basisafbeelding. |
| preservePublishState | `xsd:boolean` | Geeft aan of een vervangende afbeelding die in IPS is geüpload de bestaande instelling &quot;Klaar voor publicatie&quot; moet behouden of dat deze moet worden zoals opgegeven door het uploaden. |
| defaultSourceProfile | `types:Asset` | Hiermee wordt het standaardbronkleurprofiel (Coated FOGRA27 (ISO 126472:2004)) opgegeven dat automatisch wordt toegepast als onderdeel van het standaardkleurgedrag gebruiken bij het toevoegen van CMYK-afbeeldingsbestanden. |
| defaultDisplayProfile | `types:Asset` | Hiermee wordt het standaard interne kleurprofiel (U.S. Web Coated (SWOP) v2) opgegeven dat automatisch wordt toegepast als onderdeel van het standaardkleurgedrag gebruiken bij het toevoegen van CMYK-afbeeldingsbestanden. |
| iptcExifMappingXslt | `types:Asset` | De extractie van IPTC- en EXIF-afbeeldingskoptekstgegevens naar IPS vereist een conversie van interne veldnamen naar door de gebruiker gedefinieerde veldnamen voor het bedrijf. Hiermee wordt een XSL-vertaaltabel bepaald (de standaardinstelling is Geen IPTC- of EXIF-velden extraheren) voor geüploade afbeeldingen. |
| xmpMappingXslt | `types:Asset` | De extractie van XMP gegevens van de beeldkopbal in IPS vereist een omzetting van interne gebiedsnamen aan user-defined gebiedsnamen voor het bedrijf. Hiermee wordt een XSL-vertaaltabel bepaald (standaard is &quot;Geen XMP velden extraheren&quot;) voor geüploade afbeeldingen. |
| diskSpaceWarningMin | `xsd:int` | Minimale hoeveelheid schijfruimte voor afbeeldingsdirectory voordat een waarschuwing wordt verzonden. |
| emailTrashCleanupWarning | `xsd:boolean` | Hiermee bepaalt u of e-mailberichten worden verzonden voordat de prullenbak-items automatisch wordt verwijderd. |
| javascriptUploadEnabled | `types:Asset` | Bepaalt of JavaScript-bestanden moeten worden geüpload. Deze optie is een potentieel veiligheidsrisico, dus gebruik met zorg. |
