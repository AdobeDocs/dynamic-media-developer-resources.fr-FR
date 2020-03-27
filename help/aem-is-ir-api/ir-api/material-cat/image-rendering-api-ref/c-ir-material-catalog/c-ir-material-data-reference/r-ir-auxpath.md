---
description: Chemin d’accès au fichier de données. Chemin d’accès et nom relatifs pour les fichiers de données autres que des images associés à cette image.
seo-description: Chemin d’accès au fichier de données. Chemin d’accès et nom relatifs pour les fichiers de données autres que des images associés à cette image.
seo-title: AuxPath
solution: Experience Manager
title: AuxPath
topic: Scene7 Image Serving - Image Rendering API
uuid: 95d28f8d-27ec-480a-a62a-7e5e8fbfb3fb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# AuxPath{#auxpath}

Chemin d’accès au fichier de données. Chemin d’accès et nom relatifs pour les fichiers de données autres que des images associés à cette image.

Le serveur associe cette valeur à attribute::RootPath pour créer le chemin d’accès au fichier réel. Peut également être un chemin d’accès absolu au fichier.

Permet de spécifier un fichier de style d&#39;armoire pour un matériau d&#39;armoire ou un fichier de style de garniture de fenêtre pour un matériau de garniture de fenêtre. Laissez vide pour tous les autres matériaux.

## Propriétés {#section-4268350054b7421da0ce0327f0731a52}

Valeur de chaîne de texte. S’il est spécifié, il doit s’agir d’un chemin d’accès de fichier relatif ou absolu valide. Obligatoire pour les matériaux de l&#39;armoire et de la garniture de fenêtre. Doit être vide pour tous les autres matériaux.

## Par défaut {#section-287005c2d8e948fa958f69ba7b90b437}

Aucune

## Voir aussi {#section-e1f7a61c00d04a80af28e2e67481ab92}

[attribut::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3) , [catalogue::Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590), [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
