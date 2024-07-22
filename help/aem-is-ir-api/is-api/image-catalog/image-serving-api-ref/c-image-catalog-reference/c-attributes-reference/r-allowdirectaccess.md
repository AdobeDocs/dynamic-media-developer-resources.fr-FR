---
description: Autoriser l’accès direct aux ressources basées sur des chemins d’accès.
solution: Experience Manager
title: AllowDirectAccess
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b4000bdf-c21a-4976-82a7-70b2261dee0b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# AllowDirectAccess{#allowdirectaccess}

Autoriser l’accès direct aux ressources basées sur des chemins d’accès.

Lorsque cet attribut est défini, l’accès basé sur le chemin d’accès est autorisé ou restreint pour les types d’objets spécifiés, selon que le mot-clé `include` ou `exclude` est utilisé ou non.

>[!NOTE]
>
>Si l’attribut `AllowDirectAccess` n’est pas spécifié, la valeur par défaut est `exclude`.

* `include` autorise l’accès aux types d’objets spécifiés et restreint l’accès à tous les autres.
* `exclude` limite l’accès pour les types d’objets spécifiés et permet l’accès pour tous les autres.

Si aucun `include` ni `exclude` n&#39;est spécifié, `include` est supposé.

Les types suivants peuvent être contrôlés :

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## Exemples {#section-4c3765ebaa4245a799b454fc196f9237}

* Autoriser l’accès direct uniquement pour les types d’objets `IS` et `STATIC`

  `AllowDirectAccess=include:IS,STATIC`

* Autoriser l’accès direct pour tous les types d’objets sauf `IS` et `STATIC``AllowDirectAccess=exclude:IS,STATIC`

* Autoriser l’accès direct pour les types d’objets *no* (c’est-à-dire, n’inclure aucun)

  `AllowDirectAccess=include:`

* Autoriser l’accès direct pour les types d’objets *tous* (c’est-à-dire exclure aucun)

  `AllowDirectAccess=exclude:`

* Équivalent à `include:IS,STATIC` (si `include`/ `exclude` n&#39;est pas présent, `include` est supposé)

  `AllowDirectAccess=IS,STATIC`

  Notez qu’il s’agit de la valeur par défaut utilisée si l’attribut `AllowDirectAccess` n’est pas spécifié pour cette société.

* Inclure aucun, équivalent à `include:` (si `include`/ `exclude` n&#39;est pas présent, `include` est supposé)

  `AllowDirectAccess=`
