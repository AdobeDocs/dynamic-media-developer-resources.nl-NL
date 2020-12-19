---
description: Bepaalde inhoud die in de viewer voor draaien wordt weergegeven, is afhankelijk van lokalisatie, inclusief zoomknoppen en een knop voor volledig scherm.
seo-description: Bepaalde inhoud die in de viewer voor draaien wordt weergegeven, is afhankelijk van lokalisatie, inclusief zoomknoppen en een knop voor volledig scherm.
seo-title: Lokalisatie van gebruikersinterface-elementen
solution: Experience Manager
title: Lokalisatie van gebruikersinterface-elementen
topic: Dynamic media
uuid: bf38bdef-a31f-4f2f-a8f5-3d3d4eac95ab
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---


# Lokalisatie van gebruikersinterface-elementen{#localization-of-user-interface-elements}

Bepaalde inhoud die in de viewer voor draaien wordt weergegeven, is afhankelijk van lokalisatie, inclusief zoomknoppen en een knop voor volledig scherm.

Elke tekstinhoud in de viewer die kan worden gelokaliseerd, wordt vertegenwoordigd door een speciale viewer-SDK-id met de naam SYMBOL. Elk SYMBOL heeft een standaardtekstwaarde voor de landinstelling Engels ( `"en"`) die wordt geleverd bij de viewer buiten de box. Er kunnen ook door de gebruiker gedefinieerde waarden worden ingesteld voor zoveel landinstellingen als nodig zijn.

Wanneer de viewer wordt gestart, wordt de huidige landinstelling gecontroleerd om te zien of er een door de gebruiker gedefinieerde waarde is voor elk ondersteund SYMBOL voor de landinstelling. Als dat het geval is, gebruikt het de user-defined waarde; anders, valt het terug naar de uit-van-de-doos standaardtekst.

Door de gebruiker gedefinieerde lokalisatiegegevens kunnen als JSON-lokalisatieobject worden doorgegeven aan de viewer. Dit object bevat een lijst met ondersteunde landinstellingen, de tekstwaarden SYMBOL voor elke landinstelling en de standaardlandinstelling.

Een voorbeeld van een dergelijk lokalisatieobject is het volgende:

```
{ 
"en":{ 
"CloseButton.TOOLTIP":"Close", 
"ZoomInButton.TOOLTIP":"Zoom In" 
 }, 
 "fr":{ 
"CloseButton.TOOLTIP":"Fermer", 
"ZoomInButton.TOOLTIP":"Agrandir" 
}, 
defaultLocale:"en" 
}
```

In het bovenstaande voorbeeld definieert het lokalisatieobject twee landinstellingen ( `"en"` en `"fr"`) en biedt het lokalisatie voor twee gebruikersinterface-elementen in elke landinstelling.

De code van de webpagina moet het lokalisatieobject doorgeven aan de viewerconstructor als een waarde van het veld `localizedTexts` van het configuratieobject. Een andere optie is het doorgeven van het lokalisatieobject door de methode `setLocalizedTexts(localizationInfo)` aan te roepen.

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
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL  </span> </p> </td> 
   <td colname="col2"> <p>ARIA-label voor viewerelement op hoofdniveau. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SpinView.ROLE_DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>ARIA-rolbeschrijving voor hoofdweergavecomponent. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SpinView.USAGE_HINT  </span> </p> </td> 
   <td colname="col2"> <p>ARIA-gebruiksaanwijzingen voor toetsenbordgebruikers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Knop Sluiten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomInButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Inzoomen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomOutButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Knop Uitzoomen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomResetButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Knop Zoomen opnieuw instellen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>De knop Volledig scherm in normale toestand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>De knop Volledig scherm in volledige schermstatus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PanLeftButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Draai de linkerknop om. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PanRightButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Draai de rechterknop. </p> </td> 
  </tr> 
 </tbody> 
</table>

