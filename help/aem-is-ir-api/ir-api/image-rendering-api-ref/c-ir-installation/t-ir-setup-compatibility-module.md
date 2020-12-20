---
description: Vous devez configurer et configurer le module de compatibilité IR 3.x.
seo-description: Vous devez configurer et configurer le module de compatibilité IR 3.x.
seo-title: Configuration et configuration du module de compatibilité IR 3.x
solution: Experience Manager
title: Configuration et configuration du module de compatibilité IR 3.x
topic: Scene7 Image Serving - Image Rendering API
uuid: 609a6ac9-1a4e-4cca-ab08-aa0f957b0e31
translation-type: tm+mt
source-git-commit: a47f2b4ef8ebef0c8218dafa4678443aa61241f5
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---


# Configuration et configuration du module de compatibilité IR 3.x{#setup-and-configure-ir-x-compatibility-module}

Vous devez configurer et configurer le module de compatibilité IR 3.x.

1. Arrêter `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. Accédez au répertoire des applications Web ImageServer.
1. Copiez le contenu du répertoire [!DNL ir] dans le répertoire [!DNL ROOT].
1. Ouvrez [!DNL ROOT/WEB-INF/web.xml] dans un éditeur de texte.
1. Rechercher la ligne `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. Supprimez la mise en commentaire des balises `<servlet>` et `<servlet-mapping>`.
1. Redémarrez `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.

**Exemple Linux**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

Modifiez ensuite [!DNL web.xml]en utilisant votre éditeur favori pour annuler la mise en commentaire des balises `<servlet>` et `<servlet-mapping>`.

**Exemple Windows**

Ouvrez Explorer et accédez à `C:\Program Files\Scene7\ImageServing\webapps\ir`.

Sélectionnez tous les fichiers et dossiers et copiez-les dans `C:\Program Files\Scene7\ImageServing\webapps\ROOT`.

Modifiez ensuite le fichier `c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml`, en supprimant les commentaires des balises `<servlet>` et `<servlet-mapping>`.
