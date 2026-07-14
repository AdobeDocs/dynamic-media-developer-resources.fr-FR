---
description: La visionneuse de recherche de catalogue électronique prend en charge le rendu des icônes de zone cliquable au-dessus de la vue principale.
solution: Experience Manager
title: Prise en charge des zones cliquables
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 58e7523f-1615-4da4-bb09-a995bf427bfc
TQID: 'https://experienceleague.adobe.com/NJMiADA-R6aTQyrhd-CCP8pGFY-rjcIRfxiQ-4cRmRk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 313
ht-degree: 0%

---

# Prise en charge des zones cliquables{#image-map-support}

La visionneuse de recherche de catalogue électronique prend en charge le rendu des icônes de zone cliquable au-dessus de la vue principale.

L’aspect des icônes de carte est contrôlé par CSS, comme décrit dans la section [Effet de carte d’image](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289).

Les zones cliquables effectuent l’une des trois actions suivantes : redirection vers une page web externe, activation du panneau d’informations dans un pop-up et liens hypertexte internes.

## Rediriger vers une page web externe {#section-32ebe3c3a7f74892a428c5d48801de4d}

L’attribut `href` de la zone cliquable possède une URL vers la ressource externe, spécifiée explicitement ou encapsulée dans l’une des fonctions de modèle JavaScript prises en charge : `loadProduct()`, `loadProductCW()` et `loadProductPW()`.

Voici un exemple de redirection d’URL simple :

`href=http://www.adobe.com`

Dans cet exemple, la même URL est encapsulée avec la fonction `loadProduct()` :

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

Gardez à l’esprit que lorsque vous ajoutez le code JavaScript dans l’attribut `HREF` de votre zone cliquable, le code est exécuté sur l’ordinateur du client. Par conséquent, assurez-vous que le code JavaScript est sécurisé.

## Activation de la fenêtre contextuelle du panneau Informations {#section-7aa036420af646d1ad8cdc388add0b57}

Pour utiliser les panneaux d’informations, l’attribut `ROLLOVER_KEY` est défini pour une zone cliquable. Définissez également l’attribut `href` en même temps, sinon le traitement des URL externes interfère avec l’activation du panneau d’informations dans la pop-up.

Enfin, assurez-vous que la configuration de la visionneuse inclut les valeurs appropriées pour les paramètres `InfoPanelPopup.template` et, éventuellement, `InfoPanelPopup.infoServerUrl`.

>[!NOTE]
>
>Gardez à l’esprit que lorsque vous configurez la fenêtre contextuelle du panneau d’informations, le code HTML et le code JavaScript transmis au panneau d’informations s’exécutent sur l’ordinateur du client. Par conséquent, assurez-vous que ces codes HTML et JavaScript sont sécurisés.

## Hyperliens internes {#section-6afa4fb2fe564c429e0201f019a95849}

Cliquez sur une zone cliquable pour permuter une page à l’intérieur de la visionneuse. Pour utiliser cette fonctionnalité, un attribut `href` dans la zone cliquable possède le format spécial suivant :

` href=target: *`idx`*`

où `*`idx`*` est un index de base zéro de la répartition du catalogue.

Voici un exemple d’attribut `href` pour une zone cliquable qui pointe vers la répartition 3D dans le catalogue électronique :

`href=target:2`

