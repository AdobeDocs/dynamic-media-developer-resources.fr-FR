---
description: Utilisez ces paramètres de serveur pour SSL.
seo-description: Utilisez ces paramètres de serveur pour SSL.
seo-title: SSL
solution: Experience Manager
title: SSL
topic: Scene7 Image Serving - Image Rendering API
uuid: dec9bd09-8191-4010-8898-2890ffbe9ca7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SSL{#ssl}

Utilisez ces paramètres de serveur pour SSL.

## TC::SslPort - Port d’écoute {#section-c80eb582bf684b3fa7313a77cc606769}

Spécifie le port d’écoute du serveur de plateformes pour les connexions SSL. Valeur par défaut : 8443.

## TC::keystoreFile - Chemin du fichier de stockage de clés {#section-0cdf9b3cfcf249818b22221d01bafebe}

Spécifiez le chemin/le nom du fichier de stockage de clés SSL. Peut être un chemin absolu ou un chemin relatif à [!DNL *[!DNL install_folder]*/conf]. La valeur par défaut est *install_folder*/conf/scene7keystore.

## TC::keystorePass - Mot de passe du stockage de clés {#section-e7e9bfb7df584a248c0e3ee46803c3b1}

mot de passe du fichier de stockage des clés. Default is `scene7`.

## TC::keystoreType - Type de fichier de stockage de clés {#section-8f263e1ba67740728cd39181960d7c7d}

Sélectionnez le type de fichier de stockage des clés. &#39; `Java'` (par défaut) et &#39; `PKCS12`&#39; sont pris en charge.
