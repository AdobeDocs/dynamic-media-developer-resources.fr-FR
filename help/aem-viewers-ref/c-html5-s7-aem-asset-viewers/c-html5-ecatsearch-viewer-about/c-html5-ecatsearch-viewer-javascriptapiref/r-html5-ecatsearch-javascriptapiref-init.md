---
title: init
description: Référence de l’API JavaScript pour la visionneuse de catalogue électronique.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 4d71062c-fee7-4339-bd7f-1b7f778465c4
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 2%

---

# init{#init}

Référence de l’API JavaScript pour la visionneuse de catalogue électronique.

[!DNL `init()`]

Démarre l’initialisation de la visionneuse de catalogue électronique. À ce stade, l’élément DOM du conteneur doit être créé de sorte que le code de la visionneuse puisse le trouver à l’aide de son identifiant.

Si l’élément de conteneur ne fait pas encore partie de la mise en page de la page web (par exemple, il peut être masqué à l’aide [!DNL `display:none`] style qui lui est affecté), la visionneuse suspend son processus d’initialisation. Il le fait jusqu’au moment où la page web ramène l’élément de conteneur à la mise en page. Lorsque cet événement se produit, le chargement de la visionneuse reprend automatiquement.

N’appelez cette méthode qu’une seule fois pendant le cycle de vie de la visionneuse. Les appels suivants sont ignorés.

## Paramètres {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Aucune

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

[!DNL `{Object}`] Référence à une instance de visionneuse.

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
