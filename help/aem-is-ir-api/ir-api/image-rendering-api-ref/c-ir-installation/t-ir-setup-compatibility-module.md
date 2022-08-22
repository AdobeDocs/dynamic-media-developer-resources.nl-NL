---
title: De opstelling en vormt IR 3.x verenigbaarheidsmodule
description: Opstelling en vorm IR 3.x verenigbaarheidsmodule.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 44fbc6be-7681-402a-936a-0511e138365c
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---

# De opstelling en vormt IR 3.x verenigbaarheidsmodule{#setup-and-configure-ir-x-compatibility-module}

1. Stoppen `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. Schakel over naar de map ImageServer voor webapps.
1. Kopieer de inhoud van het dialoogvenster [!DNL ir] in de [!DNL `ROOT`] directory.
1. Openen [!DNL `ROOT/WEB-INF/web.xml`] in een teksteditor.
1. Zoeken naar de regel `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. Opmerkingen van de opmerking verwijderen `<servlet>` en `<servlet-mapping>` -tags.
1. Opnieuw starten `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.

**Linux®-voorbeeld**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

Vervolgens bewerken [!DNL `web.xml`] het gebruiken van uw favoriete redacteur om commentaren ongedaan te maken `<servlet>` en `<servlet-mapping>` -tags.

**Windows-voorbeeld**

Open Explorer en ga naar `C:\Program Files\Scene7\ImageServing\webapps\ir`.

Selecteer alle bestanden en mappen en kopieer deze naar binnen `C:\Program Files\Scene7\ImageServing\webapps\ROOT`.

Vervolgens bewerkt u het bestand `c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml`, opmerkingen over de `<servlet>` en `<servlet-mapping>` -tags.
