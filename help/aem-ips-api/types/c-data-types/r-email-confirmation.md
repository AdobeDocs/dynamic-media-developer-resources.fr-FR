---
description: Envoie un courrier électronique à un destinataire désigné en réponse à une opération cdnCacheInvalidation.
solution: Experience Manager
title: EmailConfirmation
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 5%

---


# EmailConfirmation{#emailconfirmation}

Envoie un courrier électronique à un destinataire désigné en réponse à une opération cdnCacheInvalidation.

Syntaxe

## Paramètres {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| Nom | Type | Description |
|---|---|---|
| `*`ccOriginator`*` | `xsd:boolean` | Si la valeur est true, inclut le compte utilisateur du service Web de l’utilisateur, qui est une liste de courriers électroniques désignés pour recevoir une confirmation par courrier électronique du réseau de diffusion de contenu Dynamic Media. |
| `*`ccOtherArray`*` | `types:EmailArray` | Tableau d’adresses électroniques (5 au maximum) désignées pour recevoir la notification de confirmation du réseau de diffusion de contenu Dynamic Media. |

