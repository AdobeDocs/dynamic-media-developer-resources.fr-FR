---
title: Installation et configuration du module de compatibilité IR 3.x
description: Installez et configurez le module de compatibilité IR 3.x.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 44fbc6be-7681-402a-936a-0511e138365c
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 1%

---

# Installation et configuration du module de compatibilité IR 3.x{#setup-and-configure-ir-x-compatibility-module}

1. Arrêter `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. Accédez au répertoire des applications Web ImageServer.
1. Copiez le contenu de la [!DNL ir] dans le répertoire [!DNL `ROOT`] répertoire .
1. Ouvrir [!DNL `ROOT/WEB-INF/web.xml`] dans un éditeur de texte.
1. Rechercher la ligne `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. Ne commentez pas la variable `<servlet>` et `<servlet-mapping>` balises.
1. Redémarrer `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.

**Exemple Linux®**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

Ensuite, modifiez [!DNL `web.xml`] l’utilisation de votre éditeur favori pour annuler la mise en commentaire de `<servlet>` et `<servlet-mapping>` balises.

**Exemple Windows**

Ouvrez l’Explorateur et accédez à `C:\Program Files\Scene7\ImageServing\webapps\ir`.

Sélectionnez tous les fichiers et dossiers et copiez-les dans `C:\Program Files\Scene7\ImageServing\webapps\ROOT`.

Modifiez ensuite le fichier. `c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml`, sans commentaire de la variable `<servlet>` et `<servlet-mapping>` balises.
