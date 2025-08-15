---
description: Envoie un courrier électronique à un destinataire désigné en réponse à une opération de validation cdnCacheInvalidation.
solution: Experience Manager
title: Confirmation par courrier électronique
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b4698637-a897-47fa-92d4-4ab400e56962
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 6%

---

# [!DNL EmailConfirmation]{#emailconfirmation}

Envoie un courrier électronique à un destinataire désigné en réponse à une opération de validation cdnCacheInvalidation.

Syntaxe

## Paramètres {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| Nom | Type | Description |
|---|---|---|
| ccOriginator | `xsd:boolean` | Si la valeur est true, inclut le compte d’utilisateur du service Web de l’utilisateur, qui est une liste d’e-mails désignés pour recevoir une confirmation par courrier électronique du Dynamic Media CDN. |
| ccAutresArray | `types:EmailArray` | Tableau d’adresses e-mail (5 maximum) désigné pour recevoir la notification de confirmation du Dynamic Media CDN. |
