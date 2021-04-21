---
description: Utilisez ces paramètres de serveur pour SSL.
solution: Experience Manager
title: SSL
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 4%

---


# SSL{#ssl}

Utilisez ces paramètres de serveur pour SSL.

## TC::SslPort - Port d&#39;écoute {#section-c80eb582bf684b3fa7313a77cc606769}

Spécifie le port d’écoute de Platform Server pour les connexions SSL. Valeur par défaut : 8443.

## TC::keystoreFile - Keystore File Path {#section-0cdf9b3cfcf249818b22221d01bafebe}

Spécifiez le chemin d’accès/le nom du fichier de stockage de clés SSL. Peut être un chemin absolu ou un chemin relatif à [ ! DNL *[!DNL install_folder]*/conf]. La valeur par défaut est *install_folder*/conf/scene7keystore.

## TC::keystorePass - Mot de passe de stockage de clés {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

mot de passe du fichier de stockage des clés. La valeur par défaut est `scene7`.

## TC::keystoreType - Type de stockage de clés {#section-8f263e1ba67740728cd39181960d7c7d}

Sélectionnez le type de fichier de stockage des clés. &#39; `Java'` (par défaut) et &#39; `PKCS12`&#39; sont pris en charge.
