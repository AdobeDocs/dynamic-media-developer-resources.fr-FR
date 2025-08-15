---
description: Chemin du fichier de données. Chemin et nom relatifs des fichiers de données non-images associés à cette image.
solution: Experience Manager
title: AuxPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 55f82596-72f0-48c4-9b3a-f10ea5f610f1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 3%

---

# AuxPath{#auxpath}

Chemin du fichier de données. Chemin et nom relatifs des fichiers de données non-images associés à cette image.

Le serveur combine cette valeur avec attribute::RootPath pour créer le chemin d’accès réel au fichier. Peut également être un chemin d’accès absolu au fichier.

Permet de spécifier un fichier de style d&#39;armoire pour un matériau d&#39;armoire ou un fichier de style de revêtement de fenêtre pour un matériau de revêtement de fenêtre. Laisser vide pour tous les autres matériaux.

## Propriétés {#section-4268350054b7421da0ce0327f0731a52}

Valeur de chaîne de texte. S’il est spécifié, il doit s’agir d’un chemin d’accès relatif ou absolu valide. Requis pour les matériaux d&#39;armoire et de recouvrement de fenêtre. Doit être vide pour tous les autres matériaux.

## Par défaut {#section-287005c2d8e948fa958f69ba7b90b437}

Aucune

## Voir aussi {#section-e1f7a61c00d04a80af28e2e67481ab92}

[attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3) , [catalog::Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590), [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
