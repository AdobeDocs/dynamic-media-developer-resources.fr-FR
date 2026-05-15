---
description: Autorisez l’accès direct aux ressources basées sur des chemins d’accès.
solution: Experience Manager
title: AllowDirectAccess
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b4000bdf-c21a-4976-82a7-70b2261dee0b
TQID: 'https://experienceleague.adobe.com/h2bcjdutPEZID471oI-MWfxG4trg87bIeyAxvoMyKEA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 166
ht-degree: 0%

---

# AllowDirectAccess{#allowdirectaccess}

Autorisez l’accès direct aux ressources basées sur des chemins d’accès.

Lorsque cet attribut est défini, l’accès basé sur un chemin est autorisé ou restreint pour les types d’objet spécifiés, selon que le mot-clé `include` ou `exclude` est utilisé.

>[!NOTE]
>
>Si l’attribut `AllowDirectAccess` n’est pas spécifié, la valeur par défaut est `exclude`.

* `include` autorise l&#39;accès pour les types d&#39;objet spécifiés et restreint l&#39;accès pour tous les autres.
* `exclude` limite l’accès pour les types d’objets spécifiés et autorise l’accès pour tous les autres.

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

* Autoriser l&#39;accès direct uniquement pour les types d&#39;objet `IS` et `STATIC`

  `AllowDirectAccess=include:IS,STATIC`

* Autoriser l&#39;accès direct pour tous les types d&#39;objet sauf `IS` et `STATIC` `AllowDirectAccess=exclude:IS,STATIC`

* Autoriser l&#39;accès direct pour *aucun* type d&#39;objet (c&#39;est-à-dire n&#39;en inclure aucun)

  `AllowDirectAccess=include:`

* Autoriser l&#39;accès direct pour *tous* les types d&#39;objet (c&#39;est-à-dire n&#39;en exclure aucun)

  `AllowDirectAccess=exclude:`

* Équivalent à `include:IS,STATIC` (si `include`/`exclude` n’est pas présent, `include` est supposé)

  `AllowDirectAccess=IS,STATIC`

  Notez que est la valeur par défaut qui est utilisée si l’attribut `AllowDirectAccess` n’est pas spécifié pour cette société.

* N’inclure aucun, équivalent à `include:` (si `include`/`exclude` n’est pas présent, `include` est supposé)

  `AllowDirectAccess=`
