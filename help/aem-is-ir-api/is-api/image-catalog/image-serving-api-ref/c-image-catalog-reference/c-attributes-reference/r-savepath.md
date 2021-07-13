---
description: Chemin d’accès racine pour saveToFile=. Chemin d’accès relatif du dossier racine auquel les images générées avec req=saveToFile doivent être écrites.
solution: Experience Manager
title: SavePath
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 6e2814b9-898f-4cf4-8e4f-aa972d554213
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 4%

---

# SavePath{#savepath}

Chemin d’accès racine pour saveToFile=. Chemin d’accès relatif du dossier racine auquel les images générées avec req=saveToFile doivent être écrites.

`SavePath` est une valeur de chaîne de texte.

## Propriétés {#section-343d1371e966491c92854a8df14c3c50}

Chaîne de texte. Doit être vide ou un chemin d’accès relatif au dossier valide. Toujours combiné avec le chemin racine absolu configuré avec `ImageServer::SaveDirectory`.

## Par défaut {#section-ae751eea97654f399c6aaee3f3252cbb}

Hérité de `default::SavePath` si elle n’est pas définie. L’enregistrement dans les fichiers est désactivé si la valeur résolue est vide.

## Voir aussi {#section-b38b045bbf084ca5a4b24ea12c4877ae}

[req=saveToFile](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
