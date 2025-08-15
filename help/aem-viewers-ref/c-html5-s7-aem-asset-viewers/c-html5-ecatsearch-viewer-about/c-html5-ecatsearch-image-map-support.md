---
description: La visionneuse Search catalogue électronique prend en charge le rendu des icônes de zone cliquable au-dessus de la vue principale.
solution: Experience Manager
title: Prise en charge des cartes-images
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 58e7523f-1615-4da4-bb09-a995bf427bfc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# Prise en charge des cartes-images{#image-map-support}

La visionneuse Search catalogue électronique prend en charge le rendu des icônes de zone cliquable au-dessus de la vue principale.

L’apparence des icônes de carte est contrôlée via CSS comme décrit dans [Effet](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289) de zone cliquable.

Les zones cliquables effectuent l’une des trois actions suivantes : rediriger vers une page Web externe, activer la fenêtre contextuelle du panneau d’informations et liens hypertexte internes.

## Redirection vers une page Web externe {#section-32ebe3c3a7f74892a428c5d48801de4d}

L’attribut `href` de la zone cliquable possède une URL vers la ressource externe, spécifiée explicitement ou encapsulée dans l’une des fonctions de modèle de JavaScript prises en charge : `loadProduct()`, `loadProductCW()`et `loadProductPW()`.

Voici un exemple de redirection d’URL simple :

`href=http://www.adobe.com`

Dans cet exemple, la même URL est encapsulée avec la `loadProduct()` fonction :

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

N’oubliez pas que lorsque vous ajoutez le code JavaScript dans l’attribut `HREF` de votre zone cliquable, le code est exécuté sur l’ordinateur du client. Veillez donc vous assurer que le code JavaScript est sécurisé.

## Activation de la fenêtre contextuelle du panneau d’informations {#section-7aa036420af646d1ad8cdc388add0b57}

Pour utiliser les panneaux d’informations, l’attribut d’une `ROLLOVER_KEY` zone cliquable est défini. Définissez également l’attribut `href` en même temps, sinon le traitement de l’URL externe interfère avec l’activation de la fenêtre contextuelle du panneau d’informations.

Enfin, assurez-vous que la configuration de la visionneuse inclut les valeurs appropriées et `InfoPanelPopup.template` , éventuellement, `InfoPanelPopup.infoServerUrl` les paramètres.

>[!NOTE]
>
>N’oubliez pas que lorsque vous configurez la fenêtre contextuelle du panneau d’informations, le code HTML et le code JavaScript transmis au panneau d’informations s’exécutent sur l’ordinateur du client. Par conséquent, assurez-vous que ce code HTML et JavaScript code sont sécurisés.

## Hyperliens internes {#section-6afa4fb2fe564c429e0201f019a95849}

Cliquez sur une zone cliquable pour permuter les pages internes de la visionneuse. Pour utiliser cette fonctionnalité, un `href` attribut de la zone cliquable a le format spécial suivant :

` href=target: *`IDX`*`

Où `*`IDX`*` est un index à base zéro de la planche catalogue.

Voici un `href` exemple d’attribut pour une zone cliquable qui pointe vers la planche 3D dans le catalogue électronique :

`href=target:2`
