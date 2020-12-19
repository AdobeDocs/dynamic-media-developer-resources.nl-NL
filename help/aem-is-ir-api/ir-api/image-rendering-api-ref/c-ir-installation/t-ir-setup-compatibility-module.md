---
description: U moet opstelling en de IRL 3.x verenigbaarheidsmodule vormen.
seo-description: U moet opstelling en de IRL 3.x verenigbaarheidsmodule vormen.
seo-title: De opstelling en vormt IR 3.x verenigbaarheidsmodule
solution: Experience Manager
title: De opstelling en vormt IR 3.x verenigbaarheidsmodule
topic: Scene7 Image Serving - Image Rendering API
uuid: 609a6ac9-1a4e-4cca-ab08-aa0f957b0e31
translation-type: tm+mt
source-git-commit: a47f2b4ef8ebef0c8218dafa4678443aa61241f5
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---


# Instellen en configureren van IR 3.x-compatibiliteitsmodule{#setup-and-configure-ir-x-compatibility-module}

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
