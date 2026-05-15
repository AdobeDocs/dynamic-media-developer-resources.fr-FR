---
title: Installation et configuration du module de compatibilité IR 3.x
description: Installer et configurer le module de compatibilité IR 3.x
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 44fbc6be-7681-402a-936a-0511e138365c
TQID: 'https://experienceleague.adobe.com/ce7CdClFrrIFb7fhZRKQ7XBpsNm4BTgwVFHPXy3BXhw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 95
ht-degree: 0%

---

# Installation et configuration du module de compatibilité IR 3.x{#setup-and-configure-ir-x-compatibility-module}

1. Arrêtez `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. Accédez au répertoire WebApp d’ImageServer.
1. Copiez le contenu du répertoire [!DNL ir] dans le répertoire [!DNL `ROOT`].
1. Ouvrez [!DNL `ROOT/WEB-INF/web.xml`] dans un éditeur de texte.
1. Rechercher la ligne `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. Supprimez les commentaires des balises `<servlet>` et `<servlet-mapping>`.
1. Redémarrez `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.

**Exemple Linux®**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

Modifiez ensuite les [!DNL `web.xml`] à l’aide de votre éditeur favori pour supprimer les commentaires des balises `<servlet>` et `<servlet-mapping>`.

**Exemple Windows**

Ouvrez l’Explorateur et accédez à `C:\Program Files\Scene7\ImageServing\webapps\ir`.

Sélectionnez tous les fichiers et dossiers et copiez-les dans `C:\Program Files\Scene7\ImageServing\webapps\ROOT`.

Modifiez ensuite la `c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml` du fichier, supprimant les commentaires des balises `<servlet>` et `<servlet-mapping>`.
