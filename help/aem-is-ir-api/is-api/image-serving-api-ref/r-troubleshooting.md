---
description: Cette section contient des solutions aux problèmes qui se sont parfois produits avec le serveur d’images.
solution: Experience Manager
title: Résolution des incidents
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b80d3c9a-a0c4-4944-9f91-e791a072cd5f
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---

# Résolution des incidents{#troubleshooting}

Cette section contient des solutions aux problèmes qui se sont parfois produits avec le serveur d’images.

**Généralités**

ImageServer conserve désormais un journal d’installation et un dossier de sauvegarde de tous les fichiers modifiés lors d’une installation de mise à niveau. Ce fichier et ce dossier se trouvent à la racine du répertoire d’installation Image Server.

**Au démarrage d’Image Server, le script de démarrage bloque avec le message « start pending » (LINUX uniquement)**

Cela peut indiquer un problème avec la licence Image Server, tel qu’un fichier de licence manquant ou une licence temporaire expirée. Un fichier de licence valide doit se trouver dans [!DNL /usr/local/scene7/licenses].

**Le serveur d’images bloque ou se bloque et le fichier journal du serveur d’images indique que l’espace est insuffisant ou que « ressource temporairement indisponible dans le fichier [!DNL IgcVirtualMemory.cpp]»**

La raison de ce message d’erreur est qu’Image Server n’a pas réussi à allouer la quantité de mémoire pour laquelle il a été configuré.

* Vérifiez le paramètre Mémoire physique dans [!DNL ImageServerRegistry.xml]. Il ne doit pas dépasser 50 % de moins si d’autres applications gourmandes en mémoire s’exécutent sur le même système. La valeur par défaut est de 20 %.
* Assurez-vous que l’espace d’échange sur le serveur est au moins le double de la taille de la RAM physique. Ce problème peut être à l’origine de ce problème si les paramètres d’espace d’échange sont faibles.

**L’espace disque réel utilisé par le dossier de cache dépasse ` *[!DNL cache.maxSize]*`la valeur définie dans[!DNL PlatformServer.conf]**

Cela n’indique pas l’existence d’un problème. La surcharge du système de fichiers n’est pas incluse dans le [!DNL Platform Server]paramètre de cache disque de . La quantité totale déclarée par le système peut être considérablement supérieure au paramètre. Il est recommandé de réserver deux fois plus d’espace disque que celui spécifié dans ` *[!DNL cache.maxSize]*`.

**Images rompues dans les exemples is-docs**

Ce problème se produit si le serveur d’images n’est pas en cours d’exécution. Cela se produit également si le chemin racine du catalogue ou le chemin racine de l’image a été modifié par rapport à la valeur par défaut d’installation, mais que les exemples d’images et de catalogues n’ont pas été déplacés vers les nouveaux emplacements. Vérifiez la valeur Image Server Root Path dans les fichiers de configuration. Si nécessaire, déplacez le dossier de démonstration qui contient les exemples d’images à la racine de l’image actuelle et déplacez-le [!DNL sample*.*] vers la racine du catalogue actuel.

Les exemples supposent également que certains paramètres de [!DNL default.ini] sont standard (par exemple, l’obscurcissement ou le verrouillage ne doit pas être activé).

**Trop de caches manqués après une disponibilité importante**

Selon l’utilisation du serveur, les performances peuvent être améliorées en augmentant [!DNL Platform Server] la taille du cache disque si l’espace disque est disponible. Vous pouvez modifier les paramètres en modifiant manuellement les fichiers de configuration. Voir la documentation.

**Les fichiers journaux occupent trop d’espace disque**

Le serveur d’images et [!DNL Platform Server] démarrer un nouveau fichier journal chaque jour. Par défaut, ils sont placés dans [ ! DNL *[!DNL install_root]*/ImageServing/logs]. La taille du fichier journal, le nombre de journaux conservés et le contenu du journal peuvent être configurés. Voir la documentation.

**Si un logiciel antivirus est installé sur votre serveur**

Il est recommandé de désactiver la recherche des répertoires Image Server. Sinon, l’analyse de répertoires de lecture/écriture à volume élevé (tels que le cache, les images, les polices, les profils et les répertoires de catalogue) peut entraîner des problèmes.

**Digimarc provoque des problèmes de performances pour les images de zoom**

N’utilisez pas Digimarc sur les images soumises à un zoom. La performance n’est pas acceptable. Si nécessaire, créez un catalogue distinct pour les images à utiliser pour le zoom et désactivez Digimarc pour ce catalogue.
