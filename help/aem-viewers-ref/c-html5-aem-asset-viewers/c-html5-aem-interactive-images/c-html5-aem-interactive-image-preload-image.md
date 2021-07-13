---
description: L’image de préchargement est une image d’aperçu de ressource statique qui se charge juste après avoir appelé la méthode init() et s’affiche pendant le téléchargement des bibliothèques du SDK de la visionneuse, des informations sur les ressources et les paramètres prédéfinis. L’image de préchargement a pour but d’améliorer visuellement le temps de chargement de la visionneuse et de présenter rapidement le contenu à l’utilisateur.
solution: Experience Manager
title: Image de préchargement
feature: Dynamic Media Classic,Visionneuses,SDK/API,Images interactives
role: Developer,User
exl-id: 54bea5fc-916c-4a58-bc06-b726884d488a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# Image de préchargement{#preload-image}

L’image de préchargement est une image d’aperçu de ressource statique qui se charge juste après avoir appelé la méthode init() et s’affiche pendant le téléchargement des bibliothèques du SDK de la visionneuse, des informations sur les ressources et les paramètres prédéfinis. L’image de préchargement a pour but d’améliorer visuellement le temps de chargement de la visionneuse et de présenter rapidement le contenu à l’utilisateur.

L’image de préchargement fonctionne correctement pour la méthode d’incorporation de visionneuses la plus courante, qui est l’incorporation réactive avec une hauteur illimitée. Voir l’en-tête [Intégration de conception réactive avec une hauteur libre](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

La fonctionnalité présente toutefois certaines limites lorsque d’autres méthodes d’incorporation ou des options de configuration spécifiques sont utilisées. Le rendu d’une image de préchargement peut échouer dans les cas suivants :

* Lorsque la taille de la visionneuse est fixe et que la taille est définie à l’aide de l’attribut de configuration `stagesize` dans l’enregistrement du paramètre prédéfini de la visionneuse ou dans le fichier CSS de la visionneuse externe pour l’élément de conteneur de la visionneuse de niveau supérieur.
* Lorsque l’incorporation des tailles flexibles avec la méthode d’incorporation des visionneuses définie en largeur et en hauteur est utilisée. Voir l’en-tête [Intégration de taille flexible avec largeur et hauteur définies](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Vous devrez peut-être désactiver la fonctionnalité d’image de préchargement à l’aide de l’attribut de configuration `preloadImage` si vous utilisez la visionneuse dans l’un des modes de fonctionnement répertoriés ci-dessus.

En outre, l’image de préchargement n’est pas utilisée, même si elle est activée dans la configuration, si la visionneuse est incorporée dans l’élément DOM est masquée à l’aide du paramètre CSS `display:none` ou détachée de l’arborescence DOM.
