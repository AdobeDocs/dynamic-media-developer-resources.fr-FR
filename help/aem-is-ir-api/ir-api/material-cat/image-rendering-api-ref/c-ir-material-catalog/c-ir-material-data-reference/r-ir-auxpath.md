---
description: Chemin d’accès au fichier de données. Chemin d’accès relatif et nom des fichiers de données autres que les images associés à cette image.
solution: Experience Manager
title: AuxPath
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

---


# AuxPath{#auxpath}

Chemin d’accès au fichier de données. Chemin d’accès relatif et nom des fichiers de données autres que les images associés à cette image.

Le serveur combine cette valeur avec attribut::RootPath pour créer le chemin d’accès au fichier réel. Peut également être un chemin d’accès absolu au fichier.

Utilisé pour spécifier un fichier de style d&#39;armoire pour un matériau d&#39;armoire ou un fichier de style de fenêtre pour un matériau de recouvrement de fenêtre. Laissez vide pour tous les autres matériaux.

## Propriétés {#section-4268350054b7421da0ce0327f0731a52}

Valeur de chaîne de texte. S&#39;il est spécifié, il doit s&#39;agir d&#39;un chemin d&#39;accès au fichier relatif ou absolu valide. Obligatoire pour les matériaux de l&#39;armoire et les matériaux de couverture de fenêtre. Doit être vide pour tous les autres matériaux.

## Par défaut {#section-287005c2d8e948fa958f69ba7b90b437}

Aucune

## Voir aussi {#section-e1f7a61c00d04a80af28e2e67481ab92}

[attribut ::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3) ,  [catalog::Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590),  [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
