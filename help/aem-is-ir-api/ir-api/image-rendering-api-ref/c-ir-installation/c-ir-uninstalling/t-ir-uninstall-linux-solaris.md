---
title: Désinstallation sous Linux® et Solaris™
description: Suivez ces instructions pour désinstaller le rendu d’image sur un système Linux® ou Solaris™.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c81feaba-18da-441a-bfd5-40275558a384
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 4%

---

# Désinstallation sous Linux® et Solaris™{#uninstalling-on-linux-and-solaris}

Suivez ces instructions pour désinstaller le rendu d’image sur un système Linux® ou Solaris™. Vous pouvez utiliser deux méthodes différentes. Effectuez l’une des opérations suivantes :

## Méthode 1

1. Rechercher des [!DNL uninstall.sh].

   Il se trouve dans le répertoire à partir duquel ImageRendering a été installé. Si ce répertoire a été supprimé, le package d’installation d’origine doit être décompressé et non tardif pour en extraire les [!DNL uninstall.sh].
1. Exécutez [!DNL uninstall.sh] et suivez les instructions à l’écran.

## Méthode 2

1. Arrêtez le rendu d’image avec les éléments suivants :

   ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`

1. Supprimez ImageRendering de votre système. La commande que vous utilisez dépend de votre système.
   * Linux® : `rpm -e ImageRendering`

   * Solaris™ : `pkgrm ImageRendering`

1. Supprimez tous les répertoires ou fichiers qui n’ont pas été supprimés à l’étape 2.

