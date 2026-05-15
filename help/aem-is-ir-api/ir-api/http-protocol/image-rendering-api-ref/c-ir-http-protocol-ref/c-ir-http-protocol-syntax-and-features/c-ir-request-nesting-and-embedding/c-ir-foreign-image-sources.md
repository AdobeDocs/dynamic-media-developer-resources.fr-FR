---
title: Sources d’images étrangères
description: Le service d’images prend en charge l’accès aux images sources sur des serveurs HTTP et FTP étrangers.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90f96a76-e9f3-4ad0-84af-bc0d093acf19
TQID: 'https://experienceleague.adobe.com/doS6fbVfaXGtLVNBAmOkB-TquNmOc5B2B--IewouFDY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 103
ht-degree: 0%

---

# Sources d’images étrangères{#foreign-image-sources}

Le service d’images prend en charge l’accès aux images sources sur des serveurs HTTP et FTP étrangers.

Pour spécifier une URL étrangère pour une commande `src=` ou `mask=`, il vous suffit de délimiter l’URL incorporée entière avec des accolades :

` …&src={ *[!DNL foreignUrl]*}&…`

Les URL absolues complètes (si `attribute::AllowDirectUrls` est défini) et les URL relatives aux `attribute::RootUrl` sont autorisées. Une erreur se produit si une URL absolue est incorporée et l’attribut : `AllowDirectUrls` est 0, ou si une URL relative est spécifiée et `attribute::RootUrl` est vide.

Les images étrangères sont mises en cache par le serveur en fonction des en-têtes de mise en cache inclus avec la réponse HTTP.
