---
title: Image de préchargement
description: L’image de préchargement est une image d’aperçu de ressource statique qui se charge juste après avoir appelé la méthode init() et s’affiche pendant le téléchargement des bibliothèques du SDK de la visionneuse, des ressources et des informations de paramètre prédéfini. L’image de préchargement a pour but d’améliorer visuellement le temps de chargement de la visionneuse et de présenter rapidement le contenu à l’utilisateur.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 8caf156f-d641-44e9-94f9-5ba3245061a3
source-git-commit: 4aaa77b1fb58b30b02ee15f6080169fa354d5907
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# Image de préchargement{#preload-image}

L’image de préchargement est une image d’aperçu de ressource statique qui se charge juste après avoir appelé la méthode init() et s’affiche pendant le téléchargement des bibliothèques du SDK de la visionneuse, des ressources et des informations de paramètre prédéfini. L’image de préchargement a pour but d’améliorer visuellement le temps de chargement de la visionneuse et de présenter rapidement le contenu à l’utilisateur.

L’image de préchargement fonctionne correctement pour la méthode d’incorporation de visionneuses la plus courante, qui est l’incorporation réactive avec une hauteur illimitée. Voir l’en-tête [Intégration de conception réactive avec une hauteur libre](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel.md#concept-b44f1df3c1c64d4e8b5565e7736bf95e).

La fonctionnalité présente toutefois certaines limites lorsque d’autres méthodes d’incorporation ou des options de configuration spécifiques sont utilisées. Le rendu d’une image de préchargement peut échouer dans les cas suivants :

* Lorsque la taille de la visionneuse est fixe et que la taille est définie à l’aide de l’attribut de configuration `stagesize` dans l’enregistrement du paramètre prédéfini de la visionneuse ou dans le fichier CSS de la visionneuse externe pour l’élément de conteneur de la visionneuse de niveau supérieur.
* Lors de l’utilisation de l’incorporation de tailles flexibles avec la méthode d’incorporation de visionneuses définie en largeur et en hauteur. Voir l’en-tête [Intégration de taille flexible avec largeur et hauteur définies](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Si vous utilisez la visionneuse dans l’un des modes de fonctionnement répertoriés ci-dessus, désactivez la fonction d’image de préchargement à l’aide de l’attribut de configuration `preloadImage` .

En outre, l’image de préchargement n’est pas utilisée, même si elle est activée dans la configuration, si la visionneuse est incorporée dans l’élément DOM est masquée à l’aide du paramètre CSS `display:none` ou détachée de l’arborescence DOM.
