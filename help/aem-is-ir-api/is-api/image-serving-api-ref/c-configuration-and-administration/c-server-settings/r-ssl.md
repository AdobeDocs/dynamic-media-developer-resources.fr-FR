---
description: Utilisez ces paramètres de serveur pour SSL.
solution: Experience Manager
title: SSL
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: 4a5c52cc-de47-48e0-ac92-6ee66a58a7ea
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 4%

---

# SSL{#ssl}

Utilisez ces paramètres de serveur pour SSL.

## TC::SslPort - Port d’écoute {#section-c80eb582bf684b3fa7313a77cc606769}

Spécifie le port d’écoute de Platform Server pour les connexions SSL. Valeur par défaut : 8443.

## TC::keystoreFile - Keystore File Path {#section-0cdf9b3cfcf249818b22221d01bafebe}

Spécifiez le chemin/nom du fichier de stockage de clés SSL. Il peut s’agir d’un chemin absolu ou d’un chemin relatif à [!DNL *[!DNL install_folder]*/conf]. La valeur par défaut est *install_folder*/conf/scene7keystore.

## TC::keystorePass - Keystore Password {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

mot de passe du fichier de stockage des clés. La valeur par défaut est `scene7`.

## TC::keystoreType - Keystore Type {#section-8f263e1ba67740728cd39181960d7c7d}

Sélectionnez le type de fichier de stockage des clés. &#39; `Java'` (par défaut) et &#39; `PKCS12`&#39; sont pris en charge.
