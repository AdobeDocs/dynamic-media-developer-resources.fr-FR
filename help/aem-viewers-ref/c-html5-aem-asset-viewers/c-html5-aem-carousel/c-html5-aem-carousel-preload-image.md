---
title: Précharger l’image
description: L’image de préchargement est une image d’aperçu de ressource statique qui se charge juste après avoir appelé la méthode init() et s’affiche pendant le téléchargement des bibliothèques, des ressources et des paramètres prédéfinis du SDK de la visionneuse. Le but de l’image de préchargement est d’améliorer visuellement le temps de chargement de la visionneuse et de présenter rapidement le contenu à l’utilisateur.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 8caf156f-d641-44e9-94f9-5ba3245061a3
source-git-commit: 4aaa77b1fb58b30b02ee15f6080169fa354d5907
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# Précharger l’image{#preload-image}

L’image de préchargement est une image d’aperçu de ressource statique qui se charge juste après avoir appelé la méthode init() et s’affiche pendant le téléchargement des bibliothèques, des ressources et des paramètres prédéfinis du SDK de la visionneuse. Le but de l’image de préchargement est d’améliorer visuellement le temps de chargement de la visionneuse et de présenter rapidement le contenu à l’utilisateur.

L’image de préchargement fonctionne bien pour la méthode d’incorporation de visionneuse la plus courante, qui est l’incorporation réactive avec une hauteur illimitée. Voir la rubrique [Responsive design incorporation avec une hauteur](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel.md#concept-b44f1df3c1c64d4e8b5565e7736bf95e) illimitée.

La fonctionnalité, cependant, présente certaines limitations lorsque d’autres méthodes d’incorporation ou des options de configuration spécifiques sont utilisées. Le rendu correct de l’image préchargée peut échouer dans les cas suivants :

* Lorsque la taille de la visionneuse est fixe et que la taille est définie à l’aide `stagesize` de l’attribut de configuration à l’intérieur de l’enregistrement de paramètre prédéfini de la visionneuse ou, dans le fichier CSS externe de la visionneuse pour l’élément conteneur de visionneuse de niveau supérieur.
* Lors de l’utilisation de la taille flexible, l’incorporation avec la méthode d’incorporation de la visionneuse est définie en largeur et en hauteur. Voir la rubrique [Incorporation de taille flexible avec la largeur et la hauteur définies](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Si vous utilisez la visionneuse dans l’un des modes de fonctionnement répertoriés ci-dessus, désactivez la fonction de préchargement d’image à l’aide de l’attribut `preloadImage` de configuration.

En outre, l’image de préchargement n’est pas utilisée, même si elle est activée dans la configuration, si la visionneuse est incorporée dans le DOM, l’élément est masqué à l’aide `display:none` du paramètre CSS ou détaché de l’arborescence DOM.
