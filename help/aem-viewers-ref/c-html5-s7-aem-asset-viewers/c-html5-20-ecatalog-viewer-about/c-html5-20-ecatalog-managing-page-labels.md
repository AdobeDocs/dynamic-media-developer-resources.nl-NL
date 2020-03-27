---
description: 'null'
seo-description: 'null'
seo-title: Paginalabels beheren
solution: Experience Manager
title: Paginalabels beheren
topic: Dynamic media
uuid: ab3df37d-113b-4762-ba9c-b92ffc41f1a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Paginalabels beheren{#managing-page-labels}

De gebruikersinterface van de viewer bevat twee plaatsen waar paginalabels worden weergegeven: de miniatuurmodus en het vervolgkeuzemenu van de inhoudsopgave.

Er zijn drie typen labels die kunnen worden gedefinieerd:

* Labels die door de auteur zijn gedefinieerd met behulp van het SYMBOL-lokalisatiemechanisme.
* Labels die door de auteur op de achtergrond worden gedefinieerd, in SPS.
* Labels die automatisch door de viewer worden gegenereerd.

Op SYMBOL gebaseerde labels worden gedefinieerd met behulp `MediaSet.LABEL_XX[_YY]` en `MediaSet.LABEL_DELIM` SYMBOL&#39;s, zoals beschreven in [Lokalisatie van gebruikersinterface-elementen](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74). U kunt dergelijke labels definiëren voor de hele ecatalogusspread. In dat geval moet u de korte SYMBOL-syntaxis ( `MediaSet.LABEL_XX`) gebruiken. U kunt de syntaxis ook voor elke pagina afzonderlijk opgeven met volledige SYMBOL-syntaxis ( `MediaSet.LABEL_XX_YY`).

Wanneer u labels voor beide pagina&#39;s in de catalogusspread definieert, voegt de viewer deze labels samen tot één tekenreeks met behulp van `MediaSet.LABEL_DELIM` SYMBOL. Op SYMBOL gebaseerde labels hebben voorrang op labels die op de achtergrond zijn gedefinieerd of die automatisch door de viewer worden gegenereerd.

Labels die in SPS zijn gedefinieerd, worden opgeslagen in de UserData-record van afzonderlijke paginaafbeeldingen. Hetzelfde als bij op SYMBOL gebaseerde labels. Wanneer op beide pagina&#39;s in de ecatalogusspread labels zijn gedefinieerd, worden deze dus in de liggende modus samengevoegd met `MediaSet.LABEL_DELIM` SYMBOL. SPS-labels hebben voorrang op automatisch gegenereerde labels, maar worden overschreven door op SYMBOL gebaseerde labels.

Automatisch gegenereerde labels zijn opeenvolgende nummers die zijn toegewezen aan alle pagina&#39;s in de catalogus. Automatisch gegenereerde labels worden genegeerd voor de opgegeven spread als er op SYMBOL gebaseerde labels zijn gedefinieerd of als er SPS-labels zijn gedefinieerd.

In de inhoudsopgave is het mogelijk om de weergave van automatisch gegenereerde labels met behulp van `showdefault` parameter uit te schakelen.
