---
description: Suivez ces instructions pour désinstaller Image Rendering sur un système Linux ou Solaris.
solution: Experience Manager
title: Désinstallation sous Linux et Solaris
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: c81feaba-18da-441a-bfd5-40275558a384
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# Désinstallation sous Linux et Solaris{#uninstalling-on-linux-and-solaris}

Suivez ces instructions pour désinstaller Image Rendering sur un système Linux ou Solaris.

Il existe deux façons de désinstaller Image Rendering sur un système Linux ou Solaris.

**Méthode 1**

1. Rechercher [!DNL uninstall.sh].

   Il se trouve dans le répertoire à partir duquel ImageRendering a été installé. Si ce répertoire a été supprimé, le package d’installation d’origine doit être décompressé et non chiffré pour extraire [!DNL uninstall.sh].
1. Exécutez [!DNL uninstall.sh] et suivez les instructions à l’écran.

>**Méthode 2**
>
>1. Arrêtez ImageRendering avec : ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`
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


