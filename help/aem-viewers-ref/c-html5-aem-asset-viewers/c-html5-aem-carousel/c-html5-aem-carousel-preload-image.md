---
description: L’image de préchargement est une image de de ressources statiques qui se charge juste après l’appel de la méthode init() et qui s’affiche pendant le téléchargement des bibliothèques SDK de la visionneuse, des informations sur les ressources et les paramètres prédéfinis. L’image de préchargement a pour objectif d’améliorer visuellement le temps de chargement de la visionneuse et de présenter rapidement le contenu à l’utilisateur.
seo-description: L’image de préchargement est une image de de ressources statiques qui se charge juste après l’appel de la méthode init() et qui s’affiche pendant le téléchargement des bibliothèques SDK de la visionneuse, des informations sur les ressources et les paramètres prédéfinis. L’image de préchargement a pour objectif d’améliorer visuellement le temps de chargement de la visionneuse et de présenter rapidement le contenu à l’utilisateur.
seo-title: Image de préchargement
solution: Experience Manager
title: Image de préchargement
topic: Dynamic media
uuid: bae99269-fd55-485e-b78e-873b77541d91
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Image de préchargement{#preload-image}

L’image de préchargement est une image de de ressources statiques qui se charge juste après l’appel de la méthode init() et qui s’affiche pendant le téléchargement des bibliothèques SDK de la visionneuse, des informations sur les ressources et les paramètres prédéfinis. L’image de préchargement a pour objectif d’améliorer visuellement le temps de chargement de la visionneuse et de présenter rapidement le contenu à l’utilisateur.

L’image de préchargement fonctionne correctement pour la méthode d’incorporation de visionneuse la plus courante, qui consiste à incorporer de manière réactive avec une hauteur libre. Voir l’en-tête [Incorporation de conception réactive avec une hauteur](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel.md#concept-b44f1df3c1c64d4e8b5565e7736bf95e)illimitée.

Cette fonctionnalité présente toutefois certaines limites lorsque d’autres méthodes d’incorporation ou des options de configuration spécifiques sont utilisées. Le rendu de l’image de préchargement peut échouer dans les cas suivants :

* Lorsque la taille de la visionneuse est fixe et que la taille est définie à l’aide de l’attribut `stagesize` de configuration à l’intérieur de l’enregistrement de paramètre prédéfini de la visionneuse ou dans le fichier CSS de la visionneuse externe pour l’élément  de la visionneuse de niveau supérieur.
* Lorsque la méthode d’incorporation de la taille flexible avec la largeur et la hauteur définies pour l’incorporation de la visionneuse est utilisée. Voir l’en-tête Incorporation de taille [flexible avec définition](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435)de la largeur et de la hauteur.

Vous devrez peut-être désactiver la fonction d’image de préchargement à l’aide de l’attribut `preloadImage` de configuration si vous utilisez la visionneuse dans l’un des modes de fonctionnement répertoriés ci-dessus.

En outre, l’image de préchargement n’est pas utilisée, même si elle est activée dans la configuration, si la visionneuse est incorporée dans l’élément DOM est masquée à l’aide du paramètre `display:none` CSS ou détachée de l’arborescence DOM.
