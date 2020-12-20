---
description: Envoie un courrier électronique à un destinataire désigné en réponse à une opération cdnCacheInvalidation.
seo-description: Envoie un courrier électronique à un destinataire désigné en réponse à une opération cdnCacheInvalidation.
seo-title: EmailConfirmation
solution: Experience Manager
title: EmailConfirmation
topic: Scene7 Image Production System API
uuid: c3b7aada-a03a-418d-80b2-31a86a1af786
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 5%

---


# EmailConfirmation{#emailconfirmation}

Envoie un courrier électronique à un destinataire désigné en réponse à une opération cdnCacheInvalidation.

Syntaxe

## Paramètres {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| Nom | Type | Description |
|---|---|---|
| ` *`ccOriginator`*` | `xsd:boolean` | Si la valeur est true, inclut le compte utilisateur du service Web de l’utilisateur, qui est une liste de courriers électroniques désignés pour recevoir une confirmation par courrier électronique du réseau de diffusion de contenu Scene7. |
| ` *`ccOtherArray`*` | `types:EmailArray` | Tableau d’adresses électroniques (5 au maximum) désignées pour recevoir la notification de confirmation du réseau de diffusion de contenu Scene7. |

