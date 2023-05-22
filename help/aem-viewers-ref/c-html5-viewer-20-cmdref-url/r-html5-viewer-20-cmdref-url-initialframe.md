---
title: initialFrame
description: Parameter die alle viewers gemeen hebben.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: db77edf0-e223-4f44-b83b-b6dbe5c1abd6
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---

# initialFrame{#initialframe}

Parameter die alle viewers gemeen hebben.

>[!NOTE]
>
>Deze opdracht is niet van toepassing op Video Image Viewer.

` initialFrame= *`frameIdx`*[ *`,pageIdx`*]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> frameIdx</span> </span> </p> </td> 
   <td colname="col2"> <p> Geeft een op nul gebaseerde frame-index op die de viewer tijdens het laden weergeeft. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pageIdx</span></span> </p> </td> 
   <td colname="col2"> <p>Een op nul gebaseerde index van de pagina binnen de spread wanneer het apparaat staand is. Voor een "links-naar-rechts"-omgeving: <span class="codeph"> 0</span> betekent "linkerpagina" en <span class="codeph"> 1</span> betekent "rechterpagina". Voor een "rechts-links"-omgeving is het tegenovergestelde: <span class="codeph"> 0</span> betekent "rechterpagina" en <span class="codeph"> 1</span> betekent "linkerpagina". </p> <p>Indien niet opgegeven, <span class="codeph"> 0</span> wordt standaard aangenomen. Wordt genegeerd wanneer het apparaat liggend is. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-10ee45d637134e0fbcd943c62578cb78}

Optioneel.

## Standaard {#section-d411e450028c460392cb8508f8ccc5d9}

Geen standaardwaarde.

## Voorbeeld {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
initialFrame=2
```
