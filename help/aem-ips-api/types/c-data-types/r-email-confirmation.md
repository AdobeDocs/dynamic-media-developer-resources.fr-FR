---
description: Envoie un e-mail à un destinataire désigné en réponse à une opération cdnCacheInvalidation.
solution: Experience Manager
title: Confirmation par e-mail
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b4698637-a897-47fa-92d4-4ab400e56962
TQID: 'https://experienceleague.adobe.com/h9ZZRR0zR347mzSifomCmtNW5GorTC6fgGjeSRf52KU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 78
ht-degree: 6%

---

# [!DNL EmailConfirmation]{#emailconfirmation}

Envoie un e-mail à un destinataire désigné en réponse à une opération cdnCacheInvalidation.

Syntaxe

## Paramètres {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| Nom | Type | Description |
|---|---|---|
| ccOriginator | `xsd:boolean` | Si la valeur est true, inclut le compte d’utilisateur du service web de l’utilisateur, qui est une liste d’e-mails désignés pour recevoir une confirmation par e-mail du réseau CDN Dynamic Media. |
| ccOtherArray | `types:EmailArray` | Tableau d’adresses e-mail (5 au maximum) désignées pour recevoir la notification de confirmation du réseau CDN Dynamic Media. |

