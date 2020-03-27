---
description: Bepaalde inhoud die in de Carousel Viewer wordt weergegeven, moet worden gelokaliseerd. Dit geldt ook voor knoppen voor dianavigatie.
seo-description: Bepaalde inhoud die in de Carousel Viewer wordt weergegeven, moet worden gelokaliseerd. Dit geldt ook voor knoppen voor dianavigatie.
seo-title: Lokalisatie van gebruikersinterface-elementen
solution: Experience Manager
title: Lokalisatie van gebruikersinterface-elementen
topic: Dynamic media
uuid: 82e4dc72-cc12-4ab5-8370-6270f9a3d45f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Lokalisatie van gebruikersinterface-elementen{#localization-of-user-interface-elements}

Bepaalde inhoud die in de Carousel Viewer wordt weergegeven, moet worden gelokaliseerd. Dit geldt ook voor knoppen voor dianavigatie.

Elke tekstinhoud in de viewer die kan worden gelokaliseerd, wordt vertegenwoordigd door de speciale Viewer SDK-id SYMBOL. Aan elk SYMBOL is een standaardtekstwaarde gekoppeld voor een Engelse landinstelling ( `"en"`) die wordt geleverd met de viewer buiten het vak. Bovendien kunnen er door de gebruiker gedefinieerde waarden worden ingesteld voor zoveel landinstellingen als nodig is.

Wanneer de viewer wordt gestart, wordt de huidige landinstelling gecontroleerd om te controleren of er voor elke ondersteunde SYMBOL-landinstelling een door de gebruiker gedefinieerde waarde is. Als dat het geval is, gebruikt het de user-defined waarde; anders, valt het terug naar de uit-van-de-doos standaardtekst.

Door de gebruiker gedefinieerde lokalisatiegegevens kunnen als JSON-lokalisatieobject worden doorgegeven aan de viewer. Dit object bevat een lijst met ondersteunde landinstellingen, SYMBOL-tekstwaarden voor elke landinstelling en de standaardlandinstelling.

Een voorbeeld van een dergelijk lokalisatieobject is het volgende:

```
{ 
"en":{ 
"PanLeftButton.TOOLTIP":"Left", 
"PanRightButton.TOOLTIP":"Right" 
 }, 
 "fr":{ 
"PanLeftButton.TOOLTIP":"Gauchiste", 
"PanRightButton .TOOLTIP":"Droit" 
}, 
defaultLocale:"en" 
}
```

In het bovenstaande voorbeeld definieert het lokalisatieobject twee landinstellingen ( `"en"` en `"fr"`) en biedt het lokalisatie voor twee gebruikersinterface-elementen in elke landinstelling.

De webpaginacode moet het lokalisatieobject doorgeven aan de viewerconstructor als een waarde van het `localizedTexts` veld van het configuratieobject. Een andere optie is om het lokalisatieobject door te geven door `setLocalizedTexts(localizationInfo)` methode aan te roepen.

De volgende SYMBOL&#39;s worden ondersteund:

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SYMBOOL </p> </th> 
   <th colname="col2" class="entry"> <p>Knopinfo voor... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Geselecteerde knopstatus voor afspelen pauzeren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Niet-geselecteerde knopstatus voor afspelen pauzeren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CAROUSELVIEWER_TOOLTIP_GOTO </span> </p> </td> 
   <td colname="col2"> <p> Knopinfo en ARIA-label voor vorige en volgende diaknoppen. </p> <p>Accepteert twee vervangende tokens: <span class="codeph"> $CURRENT_FRAME$ </span> voor de huidige dia-index en <span class="codeph"> $TOTAL_FRAMES$ </span> voor het totale aantal dia's. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p> ARIA-label voor viewerelement op hoofdniveau. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p> ARIA-rolbeschrijving voor hoofdweergavecomponent. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p> ARIA-gebruiksaanwijzingen voor toetsenbordgebruikers. </p> </td> 
  </tr> 
 </tbody> 
</table>

