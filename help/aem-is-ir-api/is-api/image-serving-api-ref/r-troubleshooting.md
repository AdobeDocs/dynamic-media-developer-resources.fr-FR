---
description: Cette section contient des solutions aux problèmes qui se sont parfois produits avec la diffusion d’images.
seo-description: Cette section contient des solutions aux problèmes qui se sont parfois produits avec la diffusion d’images.
seo-title: Résolution des incidents
solution: Experience Manager
title: Résolution des incidents
topic: Scene7 Image Serving - Image Rendering API
uuid: 39fdaf86-004b-4553-bde0-0367f3ef76b8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Résolution des incidents{#troubleshooting}

Cette section contient des solutions aux problèmes qui se sont parfois produits avec la diffusion d’images.

**Généraux**

ImageServer conserve désormais un journal d’installation et un dossier de sauvegarde de tous les fichiers modifiés lors d’une installation de mise à niveau. Ce fichier et ce dossier se trouvent à la racine du répertoire d’installation d’Image Serving.

**Lors du démarrage d’Image Server, le script de démarrage s’bloque avec le message &quot;en attente&quot; (LINUX uniquement).**

Cela peut indiquer un problème avec la licence de diffusion d’images, par exemple un fichier de licence manquant ou une licence temporaire expirée. Un fichier de licence valide doit se trouver dans [!DNL /usr/local/scene7/licenses].

**Image Server bloque ou se bloque et le fichier journal Image Server indique un espace insuffisant ou une &quot;ressource temporairement indisponible dans le fichier[!DNL IgcVirtualMemory.cpp]&quot;**

Ce message d’erreur s’explique par le fait que le serveur d’images n’a pas pu allouer la quantité de mémoire qu’il a été configuré pour l’utiliser.

* Vérifiez le paramètre Mémoire physique dans [!DNL ImageServerRegistry.xml]. Il ne doit pas dépasser 50 %, moins si d&#39;autres applications gourmandes en mémoire sont exécutées sur le même système. La valeur par défaut est de 20%.
* Assurez-vous que l’espace de permutation sur le serveur est au moins  la taille de la mémoire vive physique. Des paramètres d’espace de permutation faibles peuvent entraîner ce problème.

**L’espace disque utilisé par le dossier cache dépasse` *[!DNL cache.maxSize]*`défini dans[!DNL PlatformServer.conf]**

Cela n&#39;indique pas un problème. La surcharge du système de fichiers n’est pas incluse dans le paramètre de cache disque de Platform Server. Le montant total indiqué par le système peut être sensiblement supérieur au montant fixé. Il est recommandé de réserver deux fois plus d&#39;espace disque que ce qui est spécifié dans ` *[!DNL cache.maxSize]*`.

**Images rompues dans les exemples is-docs**

Cela se produit si Image Server n’est pas en cours d’exécution. Cela se produit également si le chemin racine du catalogue ou le chemin racine de l’image a été modifié depuis la valeur par défaut de l’installation, mais que les exemples d’images et de catalogues n’ont pas été déplacés vers les nouveaux emplacements. Vérifiez la valeur Chemin racine du serveur d’images dans les fichiers de configuration. Si nécessaire, déplacez le dossier de démonstration contenant les exemples d’images vers la racine de l’image active, puis accédez [!DNL sample*.*] à la racine du catalogue actuel.

Les exemples supposent également que certains paramètres [!DNL default.ini] sont standard (par exemple, l’obscurcissement ou le verrouillage ne doit pas être activé).

**Trop d’échecs de cache après une disponibilité importante**

Selon l’utilisation du serveur, les performances peuvent être améliorées en augmentant la taille du cache disque du serveur de plateformes si l’espace disque est disponible. Vous pouvez modifier les paramètres en modifiant manuellement les fichiers de configuration. Voir la documentation.

**Les fichiers journaux occupent trop d&#39;espace disque**

Le serveur Image Server et le serveur de plateformes  un nouveau fichier journal chaque jour. Par défaut, elles sont placées dans [!DNL *[!DNL install_root]*/ImageServing/logs]. La taille du fichier journal, le nombre de journaux conservés et le contenu du journal peuvent être configurés. Voir la documentation.

**Si un logiciel antivirus est installé sur votre serveur**

Il est recommandé de désactiver l’analyse des répertoires Image Serving. Sinon, l’analyse des répertoires de lecture/écriture de volume élevé (tels que le cache, les images, les polices, les  et les répertoires de catalogue) causera des problèmes.

**Digimarc entraîne des problèmes de performances pour les images de zoom**

N’utilisez pas Digimarc sur les images qui feront l’objet d’un zoom. La performance ne sera pas acceptable. Si nécessaire, créez un catalogue distinct pour les images à utiliser pour le zoom et désactivez Digimarc pour ce catalogue.
