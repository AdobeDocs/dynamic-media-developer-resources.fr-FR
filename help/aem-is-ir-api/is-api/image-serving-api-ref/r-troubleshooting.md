---
description: Cette section contient des solutions aux problèmes qui se sont produits occasionnellement avec la diffusion d’images.
solution: Experience Manager
title: Résolution des incidents
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b80d3c9a-a0c4-4944-9f91-e791a072cd5f
TQID: 'https://experienceleague.adobe.com/4m5oktRjrVv4Ro3e74fNYBgsxWfl0t7XOrGtNnCq334'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 525
ht-degree: 0%

---

# Résolution des incidents{#troubleshooting}

Cette section contient des solutions aux problèmes qui se sont produits occasionnellement avec la diffusion d’images.

**Général**

ImageServer conserve désormais un journal d’installation et un dossier de sauvegarde de tous les fichiers modifiés lors d’une installation de mise à niveau. Ce fichier et ce dossier se trouvent à la racine du répertoire d’installation du service d’images.

**Lors du démarrage du serveur d’images, le script de démarrage se bloque avec le message « démarrage en attente » (LINUX uniquement)**

Cela peut indiquer un problème avec la licence de diffusion d’images, tel qu’un fichier de licence manquant ou une licence temporaire expirée. Un fichier de licence valide doit se trouver dans [!DNL /usr/local/scene7/licenses].

**Le serveur d’images se bloque ou se bloque et le fichier journal du serveur d’images indique un espace insuffisant ou une « ressource temporairement indisponible dans le [!DNL IgcVirtualMemory.cpp] du fichier »**

La raison de ce message d’erreur est que le serveur d’images n’a pas pu allouer la quantité de mémoire qu’il a été configuré pour utiliser.

* Vérifiez le paramètre Mémoire physique dans [!DNL ImageServerRegistry.xml]. Il ne doit pas dépasser 50 %, moins si d’autres applications gourmandes en mémoire sont exécutées sur le même système. La valeur par défaut est de 20 %.
* Assurez-vous que l’espace de permutation sur le serveur est au moins deux fois plus grand que la taille de la RAM physique. Ce problème peut être dû à des paramètres d’espace de permutation faibles.

**L’espace disque réel utilisé par le dossier de cache dépasse ` *[!DNL cache.maxSize]*`défini dans[!DNL PlatformServer.conf]**

Cela n’indique pas de problème. Le surdébit du système de fichiers n’est pas inclus dans le paramètre de cache disque du [!DNL Platform Server]. La quantité totale déclarée par le système peut être sensiblement supérieure au paramètre. Il est recommandé de réserver deux fois plus d’espace disque que spécifié dans ` *[!DNL cache.maxSize]*`.

**Images endommagées dans les exemples is-docs**

Cela se produit si le serveur d’images n’est pas en cours d’exécution. Cela se produit également si le chemin d’accès racine du catalogue ou le chemin d’accès racine de l’image a été modifié à partir de la valeur d’installation par défaut, mais que les images et les catalogues d’exemple n’ont pas été déplacés vers les nouveaux emplacements. Vérifiez la valeur du Chemin racine du serveur d’images dans les fichiers de configuration. Si nécessaire, déplacez le dossier de démonstration contenant les images d’exemple vers la racine d’image actuelle, puis déplacez-[!DNL sample*.*] vers la racine de catalogue actuelle.

Les exemples supposent également que certains paramètres dans [!DNL default.ini] sont standard (par exemple, l’obfuscation ou le verrouillage ne doit pas être activé).

**Trop d’échecs du cache après une disponibilité importante**

En fonction de l’utilisation du serveur, les performances peuvent être améliorées en augmentant [!DNL Platform Server] taille du cache disque si de l’espace disque est disponible. Les paramètres peuvent être modifiés en modifiant manuellement les fichiers de configuration. Voir la documentation.

**Les fichiers journaux occupent trop d’espace disque**

Le serveur d’images et [!DNL Platform Server] lancent un nouveau fichier journal tous les jours. Par défaut, ils sont placés dans [!DNL *[!DNL install_root]*/ImageServing/logs]. La taille du fichier journal, le nombre de journaux conservés et le contenu du journal peuvent être configurés. Voir la documentation.

**Si un logiciel antivirus est installé sur votre serveur**

Il est recommandé de désactiver l’analyse des répertoires du service d’images. Dans le cas contraire, l&#39;analyse de répertoires de lecture/écriture volumineux (tels que le cache, les images, les polices, les profils et les répertoires de catalogues) peut entraîner des problèmes.

**Digimarc entraîne des problèmes de performances pour les images avec zoom**

N’utilisez pas Digimarc sur les images agrandies. Les performances ne sont pas acceptables. Si nécessaire, créez un catalogue distinct pour les images à utiliser pour le zoom et désactivez Digimarc pour ce catalogue.
