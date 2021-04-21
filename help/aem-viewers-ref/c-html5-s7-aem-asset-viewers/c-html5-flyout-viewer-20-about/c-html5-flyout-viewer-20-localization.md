---
description: Bepaalde inhoud die in de Flyout Viewer wordt weergegeven, is afhankelijk van lokalisatie. Deze inhoud bevat knopinfo voor gebruikersinterface-elementen en informatieberichten die tijdens het laden worden weergegeven in de zoomweergave voor vervolgmenu's.
solution: Experience Manager
title: Lokalisatie van gebruikersinterface-elementen
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---


# Lokalisatie van gebruikersinterface-elementen{#localization-of-user-interface-elements}

Bepaalde inhoud die in de Flyout Viewer wordt weergegeven, is afhankelijk van lokalisatie. Deze inhoud bevat knopinfo voor gebruikersinterface-elementen en informatieberichten die tijdens het laden worden weergegeven in de zoomweergave voor vervolgmenu&#39;s.

Elke tekstinhoud in de viewer die kan worden gelokaliseerd, wordt vertegenwoordigd door een speciale viewer-SDK-id met de naam SYMBOL. Elk SYMBOL heeft een standaardtekstwaarde voor de landinstelling Engels ( `"en"`) die wordt geleverd bij de viewer buiten de box. Er kunnen ook door de gebruiker gedefinieerde waarden worden ingesteld voor zoveel landinstellingen als nodig zijn.

Wanneer de viewer wordt gestart, wordt de huidige landinstelling gecontroleerd om te zien of er een door de gebruiker gedefinieerde waarde is voor elk ondersteund SYMBOL voor de landinstelling. Als dat het geval is, gebruikt het de user-defined waarde; anders, valt het terug naar de uit-van-de-doos standaardtekst.

Door de gebruiker gedefinieerde lokalisatiegegevens kunnen als JSON-lokalisatieobject worden doorgegeven aan de viewer. Dit object bevat een lijst met ondersteunde landinstellingen, SYMBOL-tekstwaarden voor elke landinstelling en de standaardlandinstelling.

Een voorbeeld van een dergelijk lokalisatieobject is het volgende:

```
{ 
"en":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Mouse over to zoom", 
"FlyoutZoomView.TIP_BUBBLE_TAP":"Tap and hold to zoom" 
 }, 
 "fr":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Passez la souris sur pour zoomer", 
"FlyoutZoomView.TIP_BUBBLE_TAP":"Appuyez et maintenez pour agrandir" 
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
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL  </span> </p> </td> 
   <td colname="col2"> <p>ARIA-label voor viewerelement op hoofdniveau. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.ROLE_DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>ARIA-rolbeschrijving voor hoofdweergavecomponent. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.USAGE_HINT  </span> </p> </td> 
   <td colname="col2"> <p>ARIA-gebruiksaanwijzingen voor toetsenbordgebruikers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_OVER  </span> </p> </td> 
   <td colname="col2"> <p>Informatiebericht voor desktopsystemen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_TAP  </span> </p> </td> 
   <td colname="col2"> <p>Informatiebericht voor aanraakapparaten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Knopinfo voor schuifknop naar links. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollRightButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Knopinfo voor knop naar rechts schuiven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Knopinfo voor knop Omhoog schuiven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Knopinfo voor schuifknop omlaag. </p> </td> 
  </tr> 
 </tbody> 
</table>

