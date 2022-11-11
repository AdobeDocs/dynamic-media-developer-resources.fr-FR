---
description: Utilisez ces paramètres de serveur pour SSL.
solution: Experience Manager
title: SSL
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 4a5c52cc-de47-48e0-ac92-6ee66a58a7ea
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 4%

---

# SSL{#ssl}

Utilisez ces paramètres de serveur pour SSL.

## TC::SslPort - Port d’écoute {#section-c80eb582bf684b3fa7313a77cc606769}

Indique le port d’écoute pour le [!DNL Platform Server] pour les connexions SSL. Valeur par défaut : 8443.

## TC::keystoreFile - Keystore File Path {#section-0cdf9b3cfcf249818b22221d01bafebe}

Spécifiez le chemin/nom du fichier de stockage de clés SSL. Peut être un chemin absolu ou un chemin relatif à [!DNL *[!DNL install_folder]*/conf]. La valeur par défaut est *install_folder*/conf/scene7keystore.

## TC::keystorePass - Keystore Password {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

mot de passe du fichier de stockage des clés. La valeur par défaut est `scene7`.

## TC::keystoreType - Keystore Type {#section-8f263e1ba67740728cd39181960d7c7d}

Sélectionnez le type de fichier de stockage des clés. &#39; `Java'` (par défaut) et &quot;&quot; `PKCS12`&#39; sont pris en charge.
