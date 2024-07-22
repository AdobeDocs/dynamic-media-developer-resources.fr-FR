---
title: Prise en charge des zones cliquables
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

# Prise en charge des zones cliquables{#image-map-support}

La visionneuse de catalogue électronique prend en charge le rendu des icônes de zone cliquable au-dessus de la vue principale.

L’aspect des icônes de carte est contrôlé via CSS, comme décrit dans la section [Effet de zone cliquable](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289).

Les zones cliquables effectuent l’une des trois actions suivantes : redirection vers une page web externe, activation contextuelle du panneau Informations et liens hypertextes internes.

## Redirection vers une page web externe {#section-32ebe3c3a7f74892a428c5d48801de4d}

L’attribut `href` de la zone cliquable comporte une URL vers la ressource externe, spécifiée explicitement ou encapsulée dans l’une des fonctions de modèle JavaScript prises en charge : `loadProduct()`, `loadProductCW()` et `loadProductPW()`.

Voici un exemple de redirection d’URL simple :

`href=http://www.adobe.com`

Dans cet exemple, la même URL est encapsulée avec la fonction `loadProduct()` :

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

Lorsque vous ajoutez le code JavaScript dans l’attribut `HREF` de votre zone cliquable, le code est exécuté sur l’ordinateur du client. Par conséquent, assurez-vous que le code JavaScript est sécurisé.

## Activation de la fenêtre contextuelle du panneau Informations {#section-7aa036420af646d1ad8cdc388add0b57}

Pour travailler avec les panneaux Informations, une zone cliquable a l’attribut `ROLLOVER_KEY` défini. En outre, définissez l’attribut `href` en même temps, sinon le traitement des URL externes interfère avec l’activation contextuelle du panneau Informations.

Enfin, assurez-vous que la configuration de la visionneuse inclut les valeurs appropriées pour les paramètres `InfoPanelPopup.template` et, éventuellement, `InfoPanelPopup.infoServerUrl` .

>[!NOTE]
>
>Lorsque vous configurez la fenêtre contextuelle du panneau d’informations, le code d’HTML et le code JavaScript transmis au panneau d’informations s’exécutent sur l’ordinateur du client. Par conséquent, assurez-vous que ce code d’HTML et ce code JavaScript sont sécurisés.

## Liens hypertextes internes {#section-6afa4fb2fe564c429e0201f019a95849}

La sélection d’une zone cliquable permet d’effectuer un échange de page interne dans la visionneuse. Pour utiliser cette fonctionnalité, un attribut `href` de la zone cliquable présente le format spécial suivant :

` href=target: *`idx`*`

Où `*`idx`*` est un index de base zéro de la diffusion du catalogue.

Voici un exemple d’attribut `href` pour une zone cliquable pointant vers la diffusion 3D dans le catalogue électronique :

`href=target:2`
