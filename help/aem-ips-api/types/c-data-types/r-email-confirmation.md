---
description: Envoie un courrier électronique à un destinataire désigné en réponse à une opération cdnCacheInvalidation.
solution: Experience Manager
title: EmailConfirmation
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 6%

---


# EmailConfirmation{#emailconfirmation}

Envoie un courrier électronique à un destinataire désigné en réponse à une opération cdnCacheInvalidation.

Syntaxe

## Paramètres {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| Nom | Type | Description |
|---|---|---|
| `*`ccOriginator`*` | `xsd:boolean` | Si la valeur est true, inclut le compte utilisateur du service Web de l’utilisateur, qui est une liste de courriers électroniques désignés pour recevoir une confirmation par courrier électronique du réseau de diffusion de contenu Dynamic Media. |
| `*`ccOtherArray`*` | `types:EmailArray` | Tableau d’adresses électroniques (5 au maximum) désignées pour recevoir la notification de confirmation du réseau de diffusion de contenu Dynamic Media. |

