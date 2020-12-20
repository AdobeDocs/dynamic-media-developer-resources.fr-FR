---
description: Chemin d’accès racine pour saveToFile=. Chemin relatif du dossier racine vers lequel les images générées avec req=saveToFile doivent être écrites.
seo-description: Chemin d’accès racine pour saveToFile=. Chemin relatif du dossier racine vers lequel les images générées avec req=saveToFile doivent être écrites.
seo-title: SavePath
solution: Experience Manager
title: SavePath
topic: Scene7 Image Serving - Image Rendering API
uuid: 02b88e83-7fee-40d4-95ea-daba9a608e8e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 3%

---


# SavePath{#savepath}

Chemin d’accès racine pour saveToFile=. Chemin relatif du dossier racine vers lequel les images générées avec req=saveToFile doivent être écrites.

`SavePath` est une valeur de chaîne de texte.

## Propriétés {#section-343d1371e966491c92854a8df14c3c50}

Chaîne de texte. Doit être vide ou un chemin d&#39;accès relatif valide au dossier. Toujours associé au chemin racine absolu configuré avec `ImageServer::SaveDirectory`.

## Par défaut {#section-ae751eea97654f399c6aaee3f3252cbb}

Hérité de `default::SavePath` si elle n&#39;est pas définie. L’enregistrement dans les fichiers est désactivé si la valeur résolue est vide.

## Voir aussi {#section-b38b045bbf084ca5a4b24ea12c4877ae}

[req=saveToFile](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
