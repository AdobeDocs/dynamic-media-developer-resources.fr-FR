---
title: init
description: Référence de l’API JavaScript pour la visionneuse de médias mixtes.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 4fb40cec-172a-41b3-98fc-927da88c7cb9
TQID: 'https://experienceleague.adobe.com/ePEFdZuRissBOT3MiTbKElPhonr9UGlR02dfN4CqUcE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 2%

---

# init{#init}

Référence de l’API JavaScript pour la visionneuse de médias mixtes.

`init()`

Démarre l’initialisation de la visionneuse de médias mixtes. À ce stade, l’élément DOM du conteneur doit être créé afin que le code de la visionneuse puisse le trouver à l’aide de son identifiant.

Si l’élément de conteneur ne fait pas encore partie de la mise en page de la page web (par exemple, il peut être masqué à l’aide du style `display:none`), la visionneuse suspend son processus d’initialisation. Elle est suspendue jusqu’au moment où la page web rétablit la mise en page de l’élément de conteneur , moment à partir duquel le chargement de la visionneuse reprend automatiquement.

N’appelez cette méthode qu’une seule fois pendant le cycle de vie de la visionneuse. Les appels suivants sont ignorés.

## Paramètres {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Aucune

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Référence à l’instance de visionneuse.

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
