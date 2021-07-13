---
description: U moet opstelling en de IRL 3.x verenigbaarheidsmodule vormen.
solution: Experience Manager
title: De opstelling en vormt IR 3.x verenigbaarheidsmodule
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 44fbc6be-7681-402a-936a-0511e138365c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 0%

---

# De opstelling en vormt IR 3.x verenigbaarheidsmodule{#setup-and-configure-ir-x-compatibility-module}

U moet opstelling en de IRL 3.x verenigbaarheidsmodule vormen.

1. Stop `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. Schakel over naar de map ImageServer voor webapps.
1. Kopieer de inhoud van de map [!DNL ir] naar de map [!DNL ROOT].
1. Open [!DNL ROOT/WEB-INF/web.xml] in een teksteditor.
1. Zoeken naar de regel `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. Verwijder de commentaarmarkeringen `<servlet>` en `<servlet-mapping>`.
1. Start `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>` opnieuw.

**Linux-voorbeeld**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

Vervolgens bewerkt u [!DNL web.xml]met uw favoriete editor om de commentaarmarkeringen `<servlet>` en `<servlet-mapping>` te verwijderen.

**Windows-voorbeeld**

Open Explorer en ga naar `C:\Program Files\Scene7\ImageServing\webapps\ir`.

Selecteer alle bestanden en mappen en kopieer deze binnen `C:\Program Files\Scene7\ImageServing\webapps\ROOT`.

Vervolgens bewerkt u het bestand `c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml` en verwijdert u de commentaarmarkeringen `<servlet>` en `<servlet-mapping>`.
