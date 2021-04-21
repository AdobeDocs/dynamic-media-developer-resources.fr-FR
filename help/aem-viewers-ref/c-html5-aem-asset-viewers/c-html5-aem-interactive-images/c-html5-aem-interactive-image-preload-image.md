---
description: L’image de préchargement est une image de prévisualisation de ressources statique qui se charge juste après avoir appelé la méthode init() et qui s’affiche pendant le téléchargement des bibliothèques du SDK de la visionneuse, des informations sur les ressources et les paramètres prédéfinis. L’objectif de l’image de préchargement est d’améliorer visuellement le temps de chargement de la visionneuse et de présenter rapidement le contenu à l’utilisateur.
solution: Experience Manager
title: Image de préchargement
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,Business Practitioner
exl-id: 54bea5fc-916c-4a58-bc06-b726884d488a
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# Précharger l’image{#preload-image}

L’image de préchargement est une image de prévisualisation de ressources statique qui se charge juste après avoir appelé la méthode init() et qui s’affiche pendant le téléchargement des bibliothèques du SDK de la visionneuse, des informations sur les ressources et les paramètres prédéfinis. L’objectif de l’image de préchargement est d’améliorer visuellement le temps de chargement de la visionneuse et de présenter rapidement le contenu à l’utilisateur.

L’image de préchargement fonctionne bien avec la méthode d’incorporation la plus courante de la visionneuse, qui consiste en une incorporation réactive avec une hauteur libre. Voir l&#39;en-tête [Incorporation de conception réactive avec une hauteur sans restriction](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Toutefois, cette fonction présente certaines limites lorsque d’autres méthodes d’incorporation ou des options de configuration spécifiques sont utilisées. Le rendu de l’image de préchargement peut échouer dans les cas suivants :

* Lorsque la taille de la visionneuse est fixe et que la taille est définie à l’aide de l’attribut de configuration `stagesize` dans l’enregistrement de paramètre prédéfini de la visionneuse ou dans le fichier CSS de la visionneuse externe pour l’élément de conteneur de la visionneuse de niveau supérieur.
* Lorsque la méthode d’incorporation de la taille flexible avec la largeur et la hauteur définie pour l’incorporation de la visionneuse est utilisée. Voir l&#39;en-tête [Intégration de taille flexible avec la largeur et la hauteur définies](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Vous devrez peut-être désactiver la fonction d’image de préchargement à l’aide de l’attribut de configuration `preloadImage` si vous utilisez la visionneuse dans l’un des modes de fonctionnement répertoriés ci-dessus.

En outre, l’image de préchargement n’est pas utilisée, même si elle est activée dans la configuration, si la visionneuse est incorporée à l’élément DOM est masquée à l’aide du paramètre CSS `display:none` ou détachée de l’arborescence DOM.
