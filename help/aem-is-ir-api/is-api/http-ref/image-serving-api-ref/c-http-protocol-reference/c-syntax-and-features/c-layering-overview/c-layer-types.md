---
description: Vier typen lagen worden ondersteund.
seo-description: Vier typen lagen worden ondersteund.
seo-title: Laagtypen
solution: Experience Manager
title: Laagtypen
topic: Scene7 Image Serving - Image Rendering API
uuid: d88b2163-7c9f-4885-9722-be3339e7127a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Laagtypen{#layer-types}

Vier typen lagen worden ondersteund.

## Afbeeldingslagen {#section-3e53df1437694272aca03f927fc0db07}

Afbeeldingslagen moeten een `src=` opdracht hebben waarmee u de afbeelding opgeeft die u als laag wilt gebruiken. U kunt een aparte afbeelding opgeven die u als laagmasker wilt gebruiken, of de afbeelding heeft al een alfakanaal. `mask=` De grootte van afbeeldingslagen wordt altijd afgeleid van de afbeelding, maar de afbeelding wordt vaak passend gemaakt met de `size=` opdracht. Er kan een clippad worden toegepast met `clipPath=`.

## Tekstlagen {#section-dc2aec6416a340bcb20c1f884323c8d0}

U moet een `text=` of `textPs=` opdracht hebben die de tekstinhoud bevat in de vorm van een RTF-tekstfragment (Rich Text Format). Tekstlagen kunnen zichzelf aanpassen aan de inhoud of worden expliciete grootten gegeven (bijvoorbeeld als tekst moet worden teruggeplaatst naar een bepaalde breedte of als de tekst moet worden beperkt binnen een bepaald gebied). `textPs=` het laten doorlopen van tekst in willekeurige vormen die zijn gedefinieerd met `textFlowPath=` en op willekeurige paden die zijn gedefinieerd met `textPath=`. `textPs=` ondersteunt ook het renderen van tekst naar het tekstvak of de opgegeven vorm onder willekeurige hoeken ( `textAngle=`).

## Effen kleurlagen {#section-56dfb672756643dda08dc93294809eb0}

Vaak worden effen kleurlagen gebruikt voor laag 0 in sjablonen, zodat de grootte van de samengestelde afbeelding vast is en onafhankelijk van de inhoud van de afbeelding. Effen kleurlagen vereisen een `color=` kenmerk en ondersteunen de meeste andere opdrachten `size=` `mask=`en kenmerken om de weergave te wijzigen. Effen kleurlagen kunnen willekeurige vormen krijgen met `clipPath=`.

## Effectlagen {#section-dd3b628bc6734077af4c0ddcebcee05f}

Laageffecten in Photoshop-stijl, zoals slagschaduwen en gloedeffecten, worden geïmplementeerd door IS met behulp van speciale sublagen die kunnen worden gekoppeld aan afbeeldings-, tekst- en effen kleurlagen. Deze effectlagen nemen het bovenliggende laagmasker en de bovenliggende laagpositie over van de bovenliggende laag en zijn beperkt in functionaliteit.
