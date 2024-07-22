---
description: Masque une partie d’une image. Le masque est toujours associé à l’image. Obtenez un masque à partir d’ImageInfo.
solution: Experience Manager
title: Masque
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0e18096c-0666-400b-a562-b6d183bd3334
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 8%

---

# [!DNL Mask]{#mask}

Masque une partie d’une image. Le masque est toujours associé à l’image. Obtenez un masque à partir d’ImageInfo.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| maskHandle | `xsd:string` | Poignée de masque. |
| nom | `xsd:string` | Nom du masque. |
| maskPath | `xsd:string` | Chemin d’accès relatif au masque. |
| maskFile | `xsd:string` | Masquer le fichier. |
| lastModified | `types:dateTime` | Date, heure et fuseau horaire de la dernière modification du masque. |
