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
ht-degree: 0%

---

# Installation et configuration du module de compatibilité IR 3.x{#setup-and-configure-ir-x-compatibility-module}

1. Arrêtez `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. Accédez au répertoire des webapps ImageServer.
1. Copiez le contenu du [!DNL ir] répertoire dans le [!DNL `ROOT`] répertoire.
1. Ouvrez [!DNL `ROOT/WEB-INF/web.xml`] dans un éditeur de texte.
1. Search de la ligne `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. Supprimez les commentaires des `<servlet>` balises et `<servlet-mapping>` .
1. Redémarrez `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.

**Exemple Linux®**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

Modifiez [!DNL `web.xml`] ensuite en utilisant votre éditeur favori pour annuler le commentaire des `<servlet>` balises et `<servlet-mapping>` .

**Exemple Windows**

Ouvrez Explorer et accédez à `C:\Program Files\Scene7\ImageServing\webapps\ir`.

Sélectionnez tous les fichiers et dossiers et copiez-les à l’intérieur `C:\Program Files\Scene7\ImageServing\webapps\ROOT`.

Modifiez ensuite le fichier `c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml`, en décommentant les `<servlet>` balises et `<servlet-mapping>` .
