---
title: init
description: Référence de l’API JavaScript pour la visionneuse Video360.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: cb543620-e774-407b-bf33-bfd2261511c4
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 2%

---

# init{#init}

Référence de l’API JavaScript pour la visionneuse Video360.

`init()`

Démarre l&#39;initialisation de la visionneuse Video360. À ce stade, l’élément DOM du conteneur doit être créé afin que le code de la visionneuse puisse le trouver à l’aide de son identifiant.

Si l’élément de conteneur ne fait pas encore partie de la mise en page de la page web (par exemple, il peut être masqué à l’aide `display:none` style qui lui est affecté), la visionneuse suspend son processus d’initialisation. Il le fait jusqu’au moment où la page web ramène l’élément de conteneur à la mise en page. Lorsque cet événement se produit, le chargement de la visionneuse reprend automatiquement.

Appelez cette méthode une seule fois pendant le cycle de vie de la visionneuse ; les appels suivants sont ignorés.

## Paramètres {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Aucune

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Référence à l’instance de visionneuse.

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
