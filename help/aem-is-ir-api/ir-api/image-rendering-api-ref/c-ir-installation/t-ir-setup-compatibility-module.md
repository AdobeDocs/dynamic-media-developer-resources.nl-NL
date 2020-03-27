---
description: U moet opstelling en de IRL 3.x verenigbaarheidsmodule vormen.
seo-description: U moet opstelling en de IRL 3.x verenigbaarheidsmodule vormen.
seo-title: De opstelling en vormt IR 3.x verenigbaarheidsmodule
solution: Experience Manager
title: De opstelling en vormt IR 3.x verenigbaarheidsmodule
topic: Scene7 Image Serving - Image Rendering API
uuid: 609a6ac9-1a4e-4cca-ab08-aa0f957b0e31
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# De opstelling en vormt IR 3.x verenigbaarheidsmodule{#setup-and-configure-ir-x-compatibility-module}

U moet opstelling en de IRL 3.x verenigbaarheidsmodule vormen.

1. Stop `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. Schakel over naar de map ImageServer voor webapps.
1. Kopieer de inhoud van de [!DNL ir] map naar de [!DNL ROOT] map.
1. Openen [!DNL ROOT/WEB-INF/web.xml] in een teksteditor.
1. Zoeken naar de regel `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. Verwijder de commentaarmarkering van de `<servlet>` tags en de `<servlet-mapping>` tags.
1. Start opnieuw `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
>**Linux-voorbeeld**
>
>`cd /usr/local/scene7/ImageServing/webapps/ROOT`
>
>`cp -r ../ir/* ./`
>
>`cd WEB-INF`
>
>Vervolgens bewerkt u de opmerkingen van de tags [!DNL web.xml]en `<servlet>` de `<servlet-mapping>` tags met behulp van uw favoriete editor.
>
>**Windows-voorbeeld**
>
>Open Verkenner en ga naar [!DNL C:\Program Files\Scene7\ImageServing\webapps\ir].
>
>Selecteer alle bestanden en mappen en kopieer deze naar binnen [!DNL C:\Program Files\Scene7\ImageServing\webapps\ROOT].
>
>Vervolgens bewerkt u het bestand [!DNL c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml]en verwijdert u de opmerkingen `<servlet>` en `<servlet-mapping>` tags.

