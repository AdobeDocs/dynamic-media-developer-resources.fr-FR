---
description: Autoriser l’accès direct aux ressources basées sur les chemins d’accès.
solution: Experience Manager
title: AllowDirectAccess
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# AllowDirectAccess{#allowdirectaccess}

Autoriser l’accès direct aux ressources basées sur les chemins d’accès.

Lorsque cet attribut est défini, l&#39;accès par chemin d&#39;accès est autorisé ou restreint pour les types d&#39;objet spécifiés, selon que le mot-clé `include` ou `exclude` est utilisé ou non.

>[!NOTE]
>
>Si l&#39;attribut `AllowDirectAccess` n&#39;est pas spécifié, la valeur par défaut est `exclude`.

* `include` permet l’accès aux types d’objets spécifiés et restreint l’accès à tous les autres.
* `exclude` restreint l’accès pour les types d’objets spécifiés et permet l’accès pour tous les autres.

Si aucun `include` ou `exclude` n&#39;est spécifié, `include` est supposé.

Les types suivants peuvent être contrôlés :

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## Exemples {#section-4c3765ebaa4245a799b454fc196f9237}

* Autoriser l&#39;accès direct uniquement pour les types d&#39;objet `IS` et `STATIC`

   `AllowDirectAccess=include:IS,STATIC`

* Autoriser l’accès direct à tous les types d’objet à l’exception de `IS` et `STATIC``AllowDirectAccess=exclude:IS,STATIC`

* Autoriser l’accès direct aux types d’objet *no* (par exemple, inclure aucun)

   `AllowDirectAccess=include:`

* Autoriser l’accès direct pour *tous les types d’objet* (c’est-à-dire exclure aucun)

   `AllowDirectAccess=exclude:`

* Équivalent à `include:IS,STATIC` (si `include`/ `exclude` n&#39;est pas présent, `include` est supposé)

   `AllowDirectAccess=IS,STATIC`

   Notez qu’il s’agit de la valeur par défaut utilisée si l’attribut `AllowDirectAccess` n’est pas spécifié pour cette société.

* Inclure aucun, équivalent à `include:` (si `include`/ `exclude` n&#39;est pas présent, `include` est supposé)

   `AllowDirectAccess=`

