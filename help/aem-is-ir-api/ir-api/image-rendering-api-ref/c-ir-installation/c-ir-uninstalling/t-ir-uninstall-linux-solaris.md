---
title: Désinstallation sous Linux® et Solaris™
description: Suivez ces instructions pour désinstaller le rendu d’image sur un système Linux® ou Solaris™.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c81feaba-18da-441a-bfd5-40275558a384
TQID: 'https://experienceleague.adobe.com/RmD5z5300Nw12kSsOretyAl5p-TeFkox-Cyqm1MrF5w'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 120
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

