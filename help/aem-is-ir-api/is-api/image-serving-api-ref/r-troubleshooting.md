---
description: Cette section contient des solutions aux problèmes qui se sont parfois produits avec Image Serving.
solution: Experience Manager
title: Résolution des incidents
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b80d3c9a-a0c4-4944-9f91-e791a072cd5f
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 1%

---

# Résolution des incidents{#troubleshooting}

Cette section contient des solutions aux problèmes qui se sont parfois produits avec Image Serving.

**Généraux**

ImageServer conserve désormais un journal d’installation et un dossier de sauvegarde de tous les fichiers modifiés lors de l’installation de la mise à niveau. Ce fichier et ce dossier se trouvent à la racine du répertoire d’installation du serveur d’images.

**Lors du démarrage du serveur d’images, le script de démarrage se bloque avec le message &quot;Démarrage en attente&quot; (LINUX uniquement).**

Cela peut indiquer un problème avec la licence de diffusion d’images, tel qu’un fichier de licence manquant ou une licence temporaire expirée. Un fichier de licence valide doit se trouver dans [!DNL /usr/local/scene7/licenses].

**Le serveur d’images bloque ou se bloque et le fichier journal du serveur d’images indique qu’il n’y a pas suffisamment d’espace ou que &quot;la ressource est temporairement indisponible dans le fichier . [!DNL IgcVirtualMemory.cpp]&quot;**

La raison de ce message d’erreur est que le serveur d’images n’a pas pu allouer la quantité de mémoire qu’il a été configuré pour utiliser.

* Vérifiez le paramètre Mémoire physique dans [!DNL ImageServerRegistry.xml]. Elle ne doit pas dépasser 50 % si d’autres applications gourmandes en mémoire sont exécutées sur le même système. La valeur par défaut est de 20%.
* Assurez-vous que l’espace de permutation sur le serveur est au moins le double de la taille de la mémoire vive physique. Les paramètres d’espace de permutation bas peuvent provoquer ce problème.

**L’espace disque réel utilisé par le dossier de cache dépasse ` *[!DNL cache.maxSize]*`set in[!DNL PlatformServer.conf]**

Cela n’indique pas de problème. La surcharge du système de fichiers n’est pas incluse dans le paramètre de cache disque du serveur Platform. Le montant total signalé par le système peut être considérablement supérieur au paramètre . Il est recommandé de réserver deux fois plus d’espace disque que celui spécifié dans ` *[!DNL cache.maxSize]*`.

**Images rompues dans les exemples is-docs**

Cela se produit si Image Server n’est pas en cours d’exécution. Cela se produit également si le chemin racine du catalogue ou le chemin racine de l’image a été modifié par défaut de l’installation, mais que les exemples d’images et de catalogues n’ont pas été déplacés vers les nouveaux emplacements. Vérifiez la valeur Chemin racine du serveur d’images dans les fichiers de configuration. Si nécessaire, déplacez le dossier de démonstration contenant les exemples d’images vers la racine de l’image active, puis déplacez [!DNL sample*.*] à la racine de catalogue actuelle.

Les exemples supposent également que certains paramètres de la variable [!DNL default.ini] sont standard (par exemple, l’obscurcissement ou le verrouillage ne doit pas être activé).

**Trop de pertes de cache après une disponibilité importante**

Selon l’utilisation du serveur, les performances peuvent être améliorées en augmentant la taille du cache disque de Platform Server si de l’espace disque est disponible. Vous pouvez modifier les paramètres en modifiant manuellement les fichiers de configuration. Voir la documentation .

**Les fichiers journaux occupent trop d’espace disque**

Le serveur d’images et le serveur de plateforme démarrent un nouveau fichier journal tous les jours. Par défaut, elles sont placées dans [!DNL *[!DNL install_root]*/ImageServing/logs]. La taille du fichier journal, le nombre de journaux conservés et le contenu du journal peuvent être configurés. Voir la documentation .

**Si un logiciel anti-virus est installé sur votre serveur**

Il est recommandé de désactiver la numérisation des répertoires de diffusion d’images. Dans le cas contraire, l’analyse de répertoires de lecture/écriture à volume élevé (tels que le cache, les images, les polices, les profils et les répertoires de catalogue) peut entraîner des problèmes.

**Digimarc entraîne des problèmes de performances pour les images de zoom.**

N’utilisez pas Digimarc sur les images agrandies. Les performances ne seront pas acceptables. Si nécessaire, créez un catalogue distinct pour les images à utiliser pour le zoom et désactivez Digimarc pour ce catalogue.
