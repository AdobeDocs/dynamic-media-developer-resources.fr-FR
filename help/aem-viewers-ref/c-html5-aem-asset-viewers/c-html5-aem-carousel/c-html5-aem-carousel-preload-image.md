---
title: Précharger l’image
description: Preload image est une image d’aperçu de ressource statique qui se charge juste après l’appel de la méthode init() et s’affiche pendant le téléchargement des bibliothèques, des ressources et des informations de paramètre prédéfini de la visionneuse SDK. L’objectif de l’image de préchargement est d’améliorer visuellement le temps de chargement de la visionneuse et de présenter rapidement le contenu à l’utilisateur.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 8caf156f-d641-44e9-94f9-5ba3245061a3
TQID: 'https://experienceleague.adobe.com/0Gm-U-1l0osVADyWyLCH4rJRUCuRHgUJ8XNsbDNpkgc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 266
ht-degree: 0%

---

# Précharger l’image{#preload-image}

Preload image est une image d’aperçu de ressource statique qui se charge juste après l’appel de la méthode init() et s’affiche pendant le téléchargement des bibliothèques, des ressources et des informations de paramètre prédéfini de la visionneuse SDK. L’objectif de l’image de préchargement est d’améliorer visuellement le temps de chargement de la visionneuse et de présenter rapidement le contenu à l’utilisateur.

Le préchargement d’image fonctionne bien avec la méthode d’incorporation de visionneuse la plus courante, qui est l’incorporation réactive avec une hauteur non limitée. Consultez l’en-tête [Incorporation en Responsive Design avec une hauteur illimitée](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel.md#concept-b44f1df3c1c64d4e8b5565e7736bf95e).

Toutefois, cette fonction présente certaines limites lorsque d’autres méthodes d’incorporation ou des options de configuration spécifiques sont utilisées. Le rendu de l’image préchargée peut échouer dans les cas suivants :

* Lorsque la taille de la visionneuse est fixe et que la taille est définie à l’aide de `stagesize`’attribut de configuration dans l’enregistrement du paramètre prédéfini de visionneuse ou, dans le fichier CSS de la visionneuse externe pour l’élément de conteneur de visionneuse de niveau supérieur.
* Lors de l’utilisation de la méthode d’incorporation de taille flexible avec largeur et hauteur définies de l’incorporation de visionneuse. Consultez l’en-tête [Incorporation de taille flexible avec définition de la largeur et de la hauteur](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435).

Si vous utilisez la visionneuse dans l’un des modes de fonctionnement répertoriés ci-dessus, désactivez la fonction de préchargement d’image à l’aide de l’attribut de configuration `preloadImage`.

En outre, l’image de préchargement n’est pas utilisée, même si elle est activée dans la configuration, si la visionneuse est incorporée dans l’élément DOM, masquée à l’aide `display:none` paramètre CSS ou détachée de l’arborescence DOM.
