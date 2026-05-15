---
description: Utilisez ces paramètres de serveur pour SSL.
solution: Experience Manager
title: SSL
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 4a5c52cc-de47-48e0-ac92-6ee66a58a7ea
TQID: 'https://experienceleague.adobe.com/VOdDIzV6b9J9AZ-qZyAj3AI77MukT1BbSzM-UM-B5N4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 86
ht-degree: 2%

---

# SSL{#ssl}

Utilisez ces paramètres de serveur pour SSL.

## TC::SslPort - Port D&#39;Écoute {#section-c80eb582bf684b3fa7313a77cc606769}

Indique le port d’écoute du [!DNL Platform Server] pour les connexions SSL. La valeur par défaut est 8443.

## TC::keystoreFile - Chemin d’accès au fichier de stockage des clés {#section-0cdf9b3cfcf249818b22221d01bafebe}

Spécifiez le chemin d’accès/nom du fichier de stockage de clés SSL. Il peut s’agir d’un chemin absolu ou d’un chemin relatif à [!DNL *[!DNL install_folder]*/conf]. La valeur par défaut est *install_folder*/conf/scene7keystore.

## TC::keystorePass - Mot de passe du KeyStore {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

Mot de passe du fichier de stockage des clés. La valeur par défaut est `scene7`.

## TC::keystoreType - Type de fichier de stockage des clés {#section-8f263e1ba67740728cd39181960d7c7d}

Sélectionnez le type de fichier de stockage des clés. &#39; `Java'` (par défaut) et &#39; `PKCS12`&#39; sont pris en charge.
