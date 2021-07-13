---
description: Il s’agit du Principal journal qui effectue le suivi de toutes les requêtes HTTP envoyées au serveur Platform. S’il est activé, le rendu d’image écrit ses données de journal d’accès dans le même fichier.
solution: Experience Manager
title: Journal d’accès
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# Journal d’accès{#access-log}

Il s’agit du Principal journal qui effectue le suivi de toutes les requêtes HTTP envoyées au serveur Platform. S’il est activé, le rendu d’image écrit ses données de journal d’accès dans le même fichier.

Le journal des accès est configuré dans server.xml.

>[!NOTE]
>
>Outre le trafic client pour la diffusion d’images ( [!DNL /is/image/*]) et le rendu d’images ( [!DNL /ir/render/*]), le journal des accès peut inclure un certain trafic interne : l’accès au système de catalogue de Platform Server ( [!DNL /is-catalog/*]), le partage du cache et les demandes de redirection d’erreur ( [!DNL /is/cache/*]), l’accès à d’autres packages déployés sur le serveur Platform, tels que les visionneuses Dynamic Media ( [!DNL /is-viewers/*]), le trafic statique et les demandes de contenu statique fournies par le serveur Platform (par exemple, [!DNL /is-docs/*]).

Les requêtes avec les chemins racine [!DNL /is-catalog] et [!DNL /is/cache] doivent toujours être exclues de toute analyse du trafic client.
