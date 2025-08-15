---
description: Autoriser l’accès direct aux ressources basées sur un chemin.
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

Autoriser l’accès direct aux ressources basées sur un chemin.

Lorsque cet attribut est défini, l’accès basé sur le chemin d’accès est autorisé ou restreint pour les types d’objet spécifiés, selon que le `include` mot-clé OU `exclude` est utilisé ou non.

>[!NOTE]
>
>Si l’attribut n’est `AllowDirectAccess` pas spécifié, la valeur par défaut est `exclude`.

* `include` Autorise l’accès pour les types d’objet spécifiés et limite l’accès pour tous les autres.
* `exclude` Limite l’accès aux types d’objet spécifiés et autorise l’accès à tous les autres.

Si ni ni n’est `include` `exclude` spécifié, `include` est supposé.

Les types suivants peuvent être contrôlés :

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## Exemples {#section-4c3765ebaa4245a799b454fc196f9237}

* Autoriser l’accès direct uniquement pour `IS` les types d’objet ET `STATIC`

  `AllowDirectAccess=include:IS,STATIC`

* Autoriser l’accès direct pour tous les types d’objet à l’exception de `IS``STATIC``AllowDirectAccess=exclude:IS,STATIC`

* Autoriser l’accès direct pour *aucun* type d’objet (c’est-à-dire n’en inclure aucun)

  `AllowDirectAccess=include:`

* Autoriser l’accès direct pour *tous les* types d’objet (c’est-à-dire n’en exclure aucun)

  `AllowDirectAccess=exclude:`

* Équivalent à `include:IS,STATIC` (si `include`/ `exclude` n’est pas présent, `include` est supposé)

  `AllowDirectAccess=IS,STATIC`

  Notez que c’est la valeur par défaut qui est utilisée si l’attribut n’est `AllowDirectAccess` pas spécifié pour cette société.

* Inclure aucun, équivalent à (si `include:`/ `include` n’est `exclude` pas présent, `include` est supposé)

  `AllowDirectAccess=`
