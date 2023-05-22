---
description: In de URL of de opeenvolging van het Bevel van de Wijzigingsbevel van de catalogus, begint een opeenvolging van de laagdefinitie met laag= bevel en eindigt met een ander layer= bevel, een effect= bevel, of het eind van URL.
solution: Experience Manager
title: Lagen opgeven
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bedd5dac-7577-4c8a-9dc3-43aa4438e53a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# Lagen opgeven{#specifying-layers}

In de URL of catalogus::Modifier bevelopeenvolging, begint een opeenvolging van de laagdefinitie met laag= bevel en eindigt met een andere layer= bevel, een effect= bevel, of het eind van URL.

Alle opdrachten in de reeks laagdefinities zijn gekoppeld aan de laag.

De `layer=` geeft een laagnummer op. Dit moet een geheel getal van 0 of meer zijn. Alle opdrachten in laagdefinitiereeksen met hetzelfde laagnummer worden op dezelfde laag toegepast. Als dezelfde opdracht meerdere keren wordt uitgevoerd, heeft de laatste instantie voorrang.
