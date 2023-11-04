---
description: Vier typen lagen worden ondersteund.
solution: Experience Manager
title: Laagtypen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9819a73d-1108-414a-831f-37ba94c3feb9
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# Laagtypen{#layer-types}

Vier typen lagen worden ondersteund.

## Afbeeldingslagen {#section-3e53df1437694272aca03f927fc0db07}

Afbeeldingslagen moeten een `src=` opdracht die de afbeelding aangeeft die als laag moet worden gebruikt. U kunt een aparte afbeelding opgeven met `mask=` die als laagmasker worden gebruikt, of de afbeelding heeft mogelijk al een alfakanaal. De grootte van afbeeldingslagen wordt altijd afgeleid van de afbeelding, maar de afbeelding wordt vaak zo geschaald dat deze past binnen de `size=` gebruiken. Er kan een clippad worden toegepast met `clipPath=`.

## Tekstlagen {#section-dc2aec6416a340bcb20c1f884323c8d0}

Moet een `text=` of `textPs=` gebruiken die de tekstinhoud bevat in de vorm van een RTF-tekstfragment (Rich Text Format). Tekstlagen kunnen zichzelf aanpassen aan de inhoud of expliciete grootten krijgen. Bijvoorbeeld als tekst moet worden teruggeplaatst naar een bepaalde breedte of als de tekst moet worden beperkt binnen een bepaald gebied. `textPs=` ondersteuning voor het laten doorlopen van tekst in willekeurige vormen gedefinieerd met `textFlowPath=` en op willekeurige paden gedefinieerd met `textPath=`. `textPs=` ondersteunt ook het renderen van tekst naar het tekstvak of de opgegeven vorm onder willekeurige hoeken ( `textAngle=`).

## Effen kleurlagen {#section-56dfb672756643dda08dc93294809eb0}

Vaak worden effen kleurlagen gebruikt voor laag 0 in sjablonen, zodat de grootte van de samengestelde afbeelding vast is en onafhankelijk van de inhoud van de afbeelding. Voor effen kleurlagen is een `color=` en `size=` of `mask=`en ondersteunt de meeste andere opdrachten en kenmerken om de weergave te wijzigen. Effen kleurlagen kunnen willekeurige vormen krijgen met `clipPath=`.

## Effectlagen {#section-dd3b628bc6734077af4c0ddcebcee05f}

Photoshop-laageffecten, zoals slagschaduwen en gloedeffecten, worden geïmplementeerd door IS met behulp van speciale sublagen die kunnen worden gekoppeld aan afbeeldings-, tekst- en effen kleurlagen. Deze effectlagen nemen het bovenliggende laagmasker en de bovenliggende laagpositie over van de bovenliggende laag en zijn beperkt in functionaliteit.
