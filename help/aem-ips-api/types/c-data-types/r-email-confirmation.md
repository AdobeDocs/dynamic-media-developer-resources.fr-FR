---
description: Envoie un courrier électronique à un destinataire désigné en réponse à une opération cdnCacheInvalidation .
solution: Experience Manager
title: EmailConfirmation
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: b4698637-a897-47fa-92d4-4ab400e56962
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 6%

---

# EmailConfirmation{#emailconfirmation}

Envoie un courrier électronique à un destinataire désigné en réponse à une opération cdnCacheInvalidation .

Syntaxe

## Paramètres {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| Nom | Type | Description |
|---|---|---|
| `*`ccOriginator`*` | `xsd:boolean` | Si la valeur est définie sur true, inclut le compte utilisateur du service Web de l’utilisateur, qui est une liste des courriers électroniques conçus pour recevoir une confirmation par courrier électronique du réseau de diffusion de contenu Dynamic Media. |
| `*`ccAutresArray`*` | `types:EmailArray` | Tableau d’adresses électroniques (5 au maximum) désignées pour recevoir la notification de confirmation du réseau de diffusion de contenu Dynamic Media. |
