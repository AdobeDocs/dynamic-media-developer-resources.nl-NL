---
description: Paginalabels beheren
solution: Experience Manager
title: Paginalabels beheren
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---


# Paginalabels beheren{#managing-page-labels}

De gebruikersinterface van de viewer bevat twee plaatsen waar paginalabels worden weergegeven: de miniatuurmodus en het vervolgkeuzemenu van de inhoudsopgave.

Er zijn drie typen labels die kunnen worden gedefinieerd:

* Labels die door de auteur zijn gedefinieerd met behulp van het SYMBOL-lokalisatiemechanisme.
* Labels die door de auteur op de achtergrond zijn gedefinieerd, in Dynamic Media Classic.
* Labels die automatisch door de viewer worden gegenereerd.

Op SYMBOL gebaseerde labels worden gedefinieerd met behulp van `MediaSet.LABEL_XX[_YY]` en `MediaSet.LABEL_DELIM` SYMBOL&#39;s zoals beschreven in [Lokalisatie van gebruikersinterface-elementen](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74). U kunt dergelijke labels definiëren voor de gehele ecatalogusspread. In dat geval moet u de korte SYMBOL-syntaxis ( `MediaSet.LABEL_XX`) gebruiken. Of geef deze voor elke pagina afzonderlijk op met volledige SYMBOL-syntaxis ( `MediaSet.LABEL_XX_YY`).

Wanneer u labels voor beide pagina&#39;s in de catalogusspread definieert, voegt de viewer deze labels samen tot één tekenreeks met behulp van SYMBOL `MediaSet.LABEL_DELIM`. Op SYMBOL gebaseerde labels hebben voorrang op labels die op de achtergrond zijn gedefinieerd of die automatisch door de viewer worden gegenereerd.

Labels die zijn gedefinieerd in Dynamic Media Classic, worden opgeslagen in de UserData-record van afzonderlijke pagina-afbeeldingen. Hetzelfde als bij op SYMBOL gebaseerde labels. Wanneer op beide pagina&#39;s in de ecatalogusspread labels zijn gedefinieerd, worden deze samengevoegd met behulp van `MediaSet.LABEL_DELIM` SYMBOL in de modus Liggend. Klassieke Dynamic Media-labels hebben voorrang op automatisch gegenereerde labels, maar worden overschreven door op SYMBOL gebaseerde labels.

Automatisch gegenereerde labels zijn opeenvolgende nummers die zijn toegewezen aan alle pagina&#39;s in de catalogus. Automatisch gegenereerde labels worden genegeerd voor de opgegeven spread als er labels op basis van SYMBOL zijn gedefinieerd of als er klassieke Dynamic Media-labels zijn gedefinieerd.

In de inhoudsopgave is het mogelijk de weergave van automatisch gegenereerde labels uit te schakelen met de parameter `showdefault`.
