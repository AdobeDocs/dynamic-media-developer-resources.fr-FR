---
description: Cette section contient des solutions aux problèmes qui se produisent parfois avec la diffusion d’images.
solution: Experience Manager
title: Résolution des incidents
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 1%

---


# Résolution des incidents{#troubleshooting}

Cette section contient des solutions aux problèmes qui se produisent parfois avec la diffusion d’images.

**Généraux**

ImageServer conserve désormais un journal d’installation et un dossier de sauvegarde de tous les fichiers modifiés lors d’une installation de mise à niveau. Ce fichier et ce dossier se trouvent à la racine du répertoire d’installation d’Image Serving.

**Lors du démarrage d’Image Server, le script de démarrage est bloqué avec le message &quot;début en attente&quot; (LINUX uniquement).**

Cela peut indiquer un problème avec la licence de diffusion d’images, tel qu’un fichier de licence manquant ou une licence temporaire expirée. Un fichier de licence valide doit être situé dans [!DNL /usr/local/scene7/licenses].

**Image Server bloque ou se bloque et le fichier journal Image Server indique qu’il n’y a pas suffisamment d’espace ou que &quot;la ressource est temporairement indisponible dans le fichier  [!DNL IgcVirtualMemory.cpp]&quot;.**

Ce message d’erreur s’explique par le fait que Image Server n’a pas pu allouer la quantité de mémoire qu’il a été configuré pour utiliser.

* Vérifiez le paramètre Mémoire physique dans [!DNL ImageServerRegistry.xml]. Il ne doit pas dépasser 50 %, moins si d&#39;autres applications gourmandes en mémoire s&#39;exécutent sur le même système. La valeur par défaut est de 20%.
* Assurez-vous que l’espace de permutation sur le serveur est au moins doublon de la taille de RAM physique. Les paramètres d’espace d’échange faibles peuvent causer ce problème.

**L&#39;espace disque réel utilisé par le dossier cache dépasse  ` *[!DNL cache.maxSize]*`défini dans[!DNL PlatformServer.conf]**

Cela n&#39;indique pas un problème. La surcharge du système de fichiers n&#39;est pas incluse dans le paramètre de cache disque de Platform Server. Le montant total indiqué par le système peut être considérablement supérieur au montant fixé. Il est recommandé de réserver deux fois plus d&#39;espace disque que celui spécifié dans ` *[!DNL cache.maxSize]*`.

**Images rompues dans les exemples is-docs**

Cela se produit si Image Server n’est pas en cours d’exécution. Elle se produit également si le chemin d’accès racine du catalogue ou le chemin d’accès racine de l’image a été modifié depuis la valeur par défaut de l’installation, mais que les exemples d’images et de catalogues n’ont pas été déplacés vers les nouveaux emplacements. Vérifiez la valeur Chemin d’accès racine du serveur d’images dans les fichiers de configuration. Si nécessaire, déplacez le dossier de démonstration contenant les exemples d’images vers la racine de l’image active, puis déplacez [!DNL sample*.*] vers la racine du catalogue actuel.

Les exemples supposent également que certains paramètres de [!DNL default.ini] sont standard (par exemple, l&#39;obscurcissement ou le verrouillage ne doit pas être activé).

**Trop d&#39;échecs de cache après un temps de disponibilité important**

En fonction de l&#39;utilisation du serveur, les performances peuvent être améliorées en augmentant la taille du cache disque du serveur de plate-forme si l&#39;espace disque est disponible. Vous pouvez modifier les paramètres en modifiant manuellement les fichiers de configuration. Voir la documentation.

**Les fichiers journaux occupent trop d&#39;espace disque**

Le serveur d’images et le serveur de plateformes début un nouveau fichier journal tous les jours. Par défaut, ils sont placés dans [ !DNL *[!DNL install_root]*/ImageServing/logs]. La taille du fichier journal, le nombre de journaux conservés et le contenu du journal peuvent être configurés. Voir la documentation.

**Si un logiciel antivirus est installé sur votre serveur**

Il est recommandé de désactiver l’analyse des répertoires Image Serving. Sinon, l’analyse des répertoires de lecture/écriture à volume élevé (tels que le cache, les images, les polices, les profils et les répertoires de catalogue) causera des problèmes.

**Digimarc entraîne des problèmes de performances pour les images de zoom**

N’utilisez pas Digimarc sur les images qui feront l’objet d’un zoom. La performance ne sera pas acceptable. Si nécessaire, créez un catalogue distinct pour les images à utiliser pour le zoom et désactivez Digimarc pour ce catalogue.
