---
title: Prise en charge des cartes-images
description: La visionneuse de catalogue électronique prend en charge le rendu des icônes de zone cliquable au-dessus de la vue principale.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 7a2a58f9-852e-4205-96bc-08332507b6cd
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 0%

---

# Prise en charge des cartes-images{#image-map-support}

La visionneuse de catalogue électronique prend en charge le rendu des icônes de zone cliquable au-dessus de la vue principale.

L’apparence des icônes de carte est contrôlée via CSS comme décrit dans [Effet](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289) de zone cliquable.

Les zones cliquables effectuent l’une des trois actions suivantes : rediriger vers une page Web externe, activer la fenêtre contextuelle du panneau d’informations et liens hypertexte internes.

## Redirection vers une page Web externe {#section-32ebe3c3a7f74892a428c5d48801de4d}

L’attribut `href` de la zone cliquable possède une URL vers la ressource externe, spécifiée explicitement ou encapsulée dans l’une des fonctions de modèle de JavaScript prises en charge : `loadProduct()`, `loadProductCW()`et `loadProductPW()`.

Voici un exemple de redirection d’URL simple :

`href=http://www.adobe.com`

Dans cet exemple, la même URL est encapsulée avec la `loadProduct()` fonction :

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

Lorsque vous ajoutez le code JavaScript dans l’attribut `HREF` de votre zone cliquable, le code est exécuté sur l’ordinateur du client. Veillez donc vous assurer que le code JavaScript est sécurisé.

## Activation de la fenêtre contextuelle du panneau d’informations {#section-7aa036420af646d1ad8cdc388add0b57}

Pour utiliser les panneaux d’informations, l’attribut d’une `ROLLOVER_KEY` zone cliquable est défini. Définissez également l’attribut `href` en même temps, sinon le traitement de l’URL externe interfère avec l’activation de la fenêtre contextuelle du panneau d’informations.

Enfin, assurez-vous que la configuration de la visionneuse inclut les valeurs appropriées et `InfoPanelPopup.template` , éventuellement, `InfoPanelPopup.infoServerUrl` les paramètres.

>[!NOTE]
>
>Lorsque vous configurez la fenêtre contextuelle du panneau d’informations, le code HTML et le code JavaScript transmis au panneau d’informations s’exécutent sur l’ordinateur du client. Par conséquent, assurez-vous que ce code HTML et JavaScript code sont sécurisés.

## Hyperliens internes {#section-6afa4fb2fe564c429e0201f019a95849}

La sélection d’une zone cliquable effectue un permutation interne de page au sein de la visionneuse. Pour utiliser cette fonctionnalité, un `href` attribut de la zone cliquable a le format spécial suivant :

` href=target: *`IDX`*`

Où `*`idx`*` est un index à base zéro de la planche catalogue.

Voici un `href` exemple d’attribut pour une zone cliquable qui pointe vers la planche 3D dans le catalogue électronique :

`href=target:2`
