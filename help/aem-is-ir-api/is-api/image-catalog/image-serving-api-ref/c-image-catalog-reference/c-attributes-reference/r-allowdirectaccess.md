---
description: Autoriser un accès direct aux ressources basées sur un chemin d’accès.
seo-description: Autoriser un accès direct aux ressources basées sur un chemin d’accès.
seo-title: AllowDirectAccess
solution: Experience Manager
title: AllowDirectAccess
topic: Scene7 Image Serving - Image Rendering API
uuid: 6d413fac-6930-4f6d-90ad-62abb419efef
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# AllowDirectAccess{#allowdirectaccess}

Autoriser un accès direct aux ressources basées sur un chemin d’accès.

Lorsque cet attribut est défini, l’accès par chemin d’accès est autorisé ou restreint pour les types d’objet spécifiés, selon que le mot-clé `include` ou `exclude` est utilisé.

>[!NOTE]
>
>Si l’ `AllowDirectAccess` attribut n’est pas spécifié, la valeur par défaut est `exclude`.

* `include` permet d’accéder aux types d’objets spécifiés et restreint l’accès à tous les autres.
* `exclude` restreint l’accès aux types d’objet spécifiés et permet l’accès à tous les autres.

Si ni `include` ni `exclude` n’est spécifié, `include` est supposé.

Les types suivants peuvent être contrôlés :

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## Exemples {#section-4c3765ebaa4245a799b454fc196f9237}

* Autoriser l’accès direct uniquement pour les types `IS` et `STATIC` d’objets

   `AllowDirectAccess=include:IS,STATIC`

* Autoriser l’accès direct à tous les types d’objet, à l’exception `IS` et `STATIC``AllowDirectAccess=exclude:IS,STATIC`

* Autoriser l’accès direct pour *aucun* type d’objet (par exemple, inclure aucun)

   `AllowDirectAccess=include:`

* Autoriser l’accès direct pour *tous les* types d’objet (c.-à-d. exclure aucun)

   `AllowDirectAccess=exclude:`

* Équivalent à `include:IS,STATIC` (si `include`/ `exclude` n’est pas présent, `include` est supposé)

   `AllowDirectAccess=IS,STATIC`

   Notez qu’il s’agit de la valeur par défaut utilisée si l’ `AllowDirectAccess` attribut n’est pas spécifié pour cette  de.

* Inclure aucune, l’équivalent `include:` (si `include`/ `exclude` n’est pas présent, `include` est supposé)

   `AllowDirectAccess=`

