---
description: L’image de préchargement est une image de prévisualisation de ressources statique qui se charge juste après avoir appelé la méthode init() et qui s’affiche pendant le téléchargement des bibliothèques du SDK de la visionneuse, des informations sur les ressources et les paramètres prédéfinis. L’objectif de l’image de préchargement est d’améliorer visuellement le temps de chargement de la visionneuse et de présenter rapidement le contenu à l’utilisateur.
seo-description: L’image de préchargement est une image de prévisualisation de ressources statique qui se charge juste après avoir appelé la méthode init() et qui s’affiche pendant le téléchargement des bibliothèques du SDK de la visionneuse, des informations sur les ressources et les paramètres prédéfinis. L’objectif de l’image de préchargement est d’améliorer visuellement le temps de chargement de la visionneuse et de présenter rapidement le contenu à l’utilisateur.
seo-title: Image de préchargement
solution: Experience Manager
title: Image de préchargement
uuid: bae99269-fd55-485e-b78e-873b77541d91
feature: Dynamic Media Classic, Visionneuses, SDK/API, Bannières de carrousel
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 0%

---


# Précharger l’image{#preload-image}

L’image de préchargement est une image de prévisualisation de ressources statique qui se charge juste après avoir appelé la méthode init() et qui s’affiche pendant le téléchargement des bibliothèques du SDK de la visionneuse, des informations sur les ressources et les paramètres prédéfinis. L’objectif de l’image de préchargement est d’améliorer visuellement le temps de chargement de la visionneuse et de présenter rapidement le contenu à l’utilisateur.

L’image de préchargement fonctionne bien avec la méthode d’incorporation la plus courante de la visionneuse, qui consiste en une incorporation réactive avec une hauteur libre. Voir l&#39;en-tête [Incorporation de conception réactive avec une hauteur sans restriction](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel.md#concept-b44f1df3c1c64d4e8b5565e7736bf95e).

Toutefois, cette fonction présente certaines limites lorsque d’autres méthodes d’incorporation ou des options de configuration spécifiques sont utilisées. Le rendu de l’image de préchargement peut échouer dans les cas suivants :

* Lorsque la taille de la visionneuse est fixe et que la taille est définie à l’aide de l’attribut de configuration `stagesize` dans l’enregistrement de paramètre prédéfini de la visionneuse ou dans le fichier CSS de la visionneuse externe pour l’élément de conteneur de la visionneuse de niveau supérieur.
* Lorsque la méthode d’incorporation de la taille flexible avec la largeur et la hauteur définie pour l’incorporation de la visionneuse est utilisée. Voir l&#39;en-tête [Intégration de taille flexible avec la largeur et la hauteur définies](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Vous devrez peut-être désactiver la fonction d’image de préchargement à l’aide de l’attribut de configuration `preloadImage` si vous utilisez la visionneuse dans l’un des modes de fonctionnement répertoriés ci-dessus.

En outre, l’image de préchargement n’est pas utilisée, même si elle est activée dans la configuration, si la visionneuse est incorporée à l’élément DOM est masquée à l’aide du paramètre CSS `display:none` ou détachée de l’arborescence DOM.
