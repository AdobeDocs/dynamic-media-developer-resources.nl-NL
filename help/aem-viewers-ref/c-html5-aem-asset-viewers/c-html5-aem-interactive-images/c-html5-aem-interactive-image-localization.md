---
description: Bepaalde inhoud die in de Interactive Image Viewer wordt weergegeven, is afhankelijk van lokalisatie. Dit omvat knopinfo voor gebruikersinterface-elementen en een informatiebericht dat tijdens het laden wordt weergegeven in de zoomweergave voor vervolgmenu's.
title: Lokalisatie van gebruikersinterface-elementen
feature: Dynamic Media Classic,Viewers,SDK/API,Interactieve afbeeldingen
role: Ontwikkelaar,zakelijke praktiserer
exl-id: 19749c74-5c31-4dcf-ab07-0e7f10176a86
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# Lokalisatie van gebruikersinterface-elementen{#localization-of-user-interface-elements}

Bepaalde inhoud die in de Interactive Image Viewer wordt weergegeven, is afhankelijk van lokalisatie. Dit omvat knopinfo voor gebruikersinterface-elementen en een informatiebericht dat tijdens het laden wordt weergegeven in de zoomweergave voor vervolgmenu&#39;s.

Elke tekstinhoud in de viewer die kan worden gelokaliseerd, wordt vertegenwoordigd door de speciale Viewer SDK-id SYMBOL. Elk SYMBOL heeft een aan de standaard gekoppelde tekstwaarde voor een Engelse landinstelling ( `"en"`) die wordt geleverd met de viewer buiten de box en kan ook door de gebruiker gedefinieerde waarden hebben ingesteld voor zoveel landinstellingen als nodig.

Wanneer de viewer wordt gestart, wordt de huidige landinstelling gecontroleerd om te controleren of er voor elke ondersteunde SYMBOL-landinstelling een door de gebruiker gedefinieerde waarde is. Als dat het geval is, gebruikt het de user-defined waarde; anders, valt het terug naar de uit-van-de-doos standaardtekst.

Door de gebruiker gedefinieerde lokalisatiegegevens kunnen als JSON-lokalisatieobject worden doorgegeven aan de viewer. Dit object bevat een lijst met ondersteunde landinstellingen, SYMBOL-tekstwaarden voor elke landinstelling en de standaardlandinstelling.

Een voorbeeld van een dergelijk lokalisatieobject is het volgende:

```
{ 
"en":{ 
"Container.LABEL":"Interactive Image Viewer" 
 }, 
 "fr":{ 
"Container.LABEL":"Visionneuse d'images interactive" 
}, 
defaultLocale:"en" 
}
```

In het bovenstaande voorbeeld definieert het lokalisatieobject twee landinstellingen ( `"en"` en `"fr"`) en biedt het lokalisatie voor twee gebruikersinterface-elementen in elke landinstelling.

De code van de webpagina moet het lokalisatieobject doorgeven aan de viewerconstructor als een waarde van het veld `localizedTexts` van het configuratieobject. Een andere optie is om het lokalisatieobject door te geven door de methode `setLocalizedTexts(localizationInfo)` aan te roepen.

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
   <td colname="col1"> <p> <span class="codeph"> ZoomView.ROLE_DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>ARIA-rolbeschrijving voor hoofdweergavecomponent. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT  </span> </p> </td> 
   <td colname="col2"> <p>ARIA-gebruiksaanwijzingen voor toetsenbordgebruikers. </p> </td> 
  </tr> 
 </tbody> 
</table>
