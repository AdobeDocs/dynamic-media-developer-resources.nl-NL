---
description: Paginalabels beheren
solution: Experience Manager
title: Paginalabels beheren
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 73c3904f-678f-47c4-b895-86671402df79
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# Paginalabels beheren{#managing-page-labels}

De gebruikersinterface van de viewer bevat twee plaatsen waar paginalabels worden weergegeven: de miniatuurmodus en het vervolgkeuzemenu van de inhoudsopgave.

Er zijn drie typen labels die kunnen worden gedefinieerd:

* Labels die door de auteur zijn gedefinieerd met behulp van het SYMBOL-lokalisatiemechanisme.
* Labels die door de auteur op de achtergrond zijn gedefinieerd, in Dynamic Media Classic.
* Labels die automatisch door de viewer worden gegenereerd.

Op SYMBOL gebaseerde labels worden gedefinieerd met `MediaSet.LABEL_XX[_YY]` en `MediaSet.LABEL_DELIM` SYMBOLEN zoals beschreven in [Lokalisatie van gebruikersinterface-elementen](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74). U kunt dergelijke labels definiëren voor de hele ecatalogusspread. In dat geval moet u de korte SYMBOL-syntaxis gebruiken ( `MediaSet.LABEL_XX`). U kunt ook voor elke pagina afzonderlijk opgeven met volledige SYMBOL-syntaxis ( `MediaSet.LABEL_XX_YY`).

Wanneer u labels voor beide pagina&#39;s in de catalogusspread definieert, voegt de viewer deze labels samen tot één tekenreeks met `MediaSet.LABEL_DELIM` SYMBOOL. Op SYMBOL gebaseerde labels hebben voorrang op labels die op de achtergrond zijn gedefinieerd of die automatisch door de viewer worden gegenereerd.

Labels die in Dynamic Media Classic zijn gedefinieerd, worden opgeslagen in de UserData-record van afzonderlijke pagina-afbeeldingen. Hetzelfde als bij op SYMBOL gebaseerde labels. Wanneer op beide pagina&#39;s in de ecatalogusspread labels zijn gedefinieerd, worden deze samengevoegd met `MediaSet.LABEL_DELIM` SYMBOL in de modus Liggend. Dynamic Media Classic-labels hebben voorrang op automatisch gegenereerde labels, maar worden overschreven door SYMBOL-labels.

Automatisch gegenereerde labels zijn opeenvolgende nummers die zijn toegewezen aan alle pagina&#39;s in de catalogus. Automatisch gegenereerde labels worden genegeerd voor de opgegeven spread als er op SYMBOL gebaseerde labels zijn gedefinieerd of als er Dynamic Media Classic-labels zijn gedefinieerd.

In de inhoudsopgave kunt u de weergave van automatisch gegenereerde labels uitschakelen met `showdefault` parameter.
