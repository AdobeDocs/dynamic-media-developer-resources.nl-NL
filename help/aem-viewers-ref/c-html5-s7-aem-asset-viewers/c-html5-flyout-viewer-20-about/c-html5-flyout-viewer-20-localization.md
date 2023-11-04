---
title: Lokalisatie van gebruikersinterface-elementen
description: Bepaalde inhoud die in de Flyout Viewer wordt weergegeven, is afhankelijk van lokalisatie. Deze inhoud bevat knopinfo voor gebruikersinterface-elementen en informatieberichten die tijdens het laden worden weergegeven in de zoomweergave voor vervolgmenu's.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 57941e90-1462-43e6-80db-6b111e004f9b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# Lokalisatie van gebruikersinterface-elementen{#localization-of-user-interface-elements}

Bepaalde inhoud die in de Flyout Viewer wordt weergegeven, is afhankelijk van lokalisatie. Deze inhoud bevat knopinfo voor gebruikersinterface-elementen en informatieberichten die tijdens het laden worden weergegeven in de zoomweergave voor vervolgmenu&#39;s.

Elke tekstinhoud in de viewer die kan worden gelokaliseerd, wordt vertegenwoordigd door een speciale viewer-SDK-id met de naam SYMBOL. Elk SYMBOL heeft een aan de standaardwaarde gekoppelde tekstwaarde voor de landinstelling Engels ( `"en"`) wordt geleverd bij de viewer buiten de box. Er kunnen ook door de gebruiker gedefinieerde waarden worden ingesteld voor het aantal landinstellingen dat nodig is.

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

In het bovenstaande voorbeeld definieert het lokalisatieobject twee landinstellingen ( `"en"` en `"fr"`) en biedt lokalisatie voor twee gebruikersinterface-elementen in elke landinstelling.

De webpaginacode moet het lokalisatieobject doorgeven aan de viewerconstructor, als een waarde van de `localizedTexts` veld van het configuratieobject. Een andere mogelijkheid is om het lokalisatieobject door te geven door het `setLocalizedTexts(localizationInfo)` methode.

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
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p>ARIA-label voor viewerelement op het hoogste niveau. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>ARIA-rolbeschrijving voor hoofdweergavecomponent. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>ARIA-gebruiksaanwijzingen voor toetsenbordgebruikers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_OVER </span> </p> </td> 
   <td colname="col2"> <p>Informatiebericht voor desktopsystemen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_TAP </span> </p> </td> 
   <td colname="col2"> <p>Informatie voor aanraakapparaten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Knopinfo voor schuifknop naar links. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Knopinfo voor knop naar rechts schuiven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Knopinfo voor schuifknop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Knopinfo voor schuifknop omlaag. </p> </td> 
  </tr> 
 </tbody> 
</table>
