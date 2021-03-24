---
description: Suivez ces instructions pour désinstaller Image Rendering sur un système Linux ou Solaris.
solution: Experience Manager
title: Désinstallation sous Linux et Solaris
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---


# Désinstallation sous Linux et Solaris{#uninstalling-on-linux-and-solaris}

Suivez ces instructions pour désinstaller Image Rendering sur un système Linux ou Solaris.

Il existe deux manières de désinstaller Image Rendering sur un système Linux ou Solaris.

**Méthode 1**

1. Rechercher [!DNL uninstall.sh].

   Il se trouve dans le répertoire d’où ImageRendering a été installé. Si ce répertoire a été supprimé, le package d&#39;installation d&#39;origine doit être décompressé et non taré pour extraire [!DNL uninstall.sh].
1. Exécutez [!DNL uninstall.sh] et suivez les instructions affichées à l’écran.

>**Méthode 2**
>
>1. Arrêter ImageRendering avec : ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`
>1. Supprimez ImageRendering de votre système.

>
>   
La commande de suppression d’ImageRendering dépend de votre système :
>
>   Linux : `rpm -e ImageRendering`
>
>   Solaris : `pkgrm ImageRendering`
>
>1. Supprimez tous les répertoires ou fichiers qui n’ont pas été supprimés à l’étape 2.

>



