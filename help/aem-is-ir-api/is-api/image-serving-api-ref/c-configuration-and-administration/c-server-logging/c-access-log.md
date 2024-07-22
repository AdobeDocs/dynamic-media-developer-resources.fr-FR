---
description: Il s’agit du journal principal qui effectue le suivi de toutes les requêtes HTTP envoyées à l’ [!DNL Platform Server]. S’il est activé, le rendu d’image écrit ses données de journal d’accès dans le même fichier.
solution: Experience Manager
title: Journal d’accès
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---

# Journal d’accès{#access-log}

Il s’agit du journal principal qui effectue le suivi de toutes les requêtes HTTP effectuées sur le [!DNL Platform Server]. S’il est activé, le rendu d’image écrit ses données de journal d’accès dans le même fichier.

Le journal des accès est configuré dans server.xml.

>[!NOTE]
>
>Outre le trafic client pour le service d’images ( [!DNL /is/image/*]) et le rendu d’images ( [!DNL /ir/render/*]), le journal d’accès peut inclure un certain trafic interne : accès au système de catalogues [!DNL Platform Server] ( [!DNL /is-catalog/*]), partage de cache et demandes de redirection d’erreur ( [!DNL /is/cache/*]), accès à d’autres packages déployés sur [!DNL Platform Server], tels que les visionneuses Dynamic Media ( [!DNL /is-viewers/*]), ainsi que les demandes de trafic statiques et de contenu traité par l’ [!DNL Platform Server] (exemple) (par exemple). , [!DNL /is-docs/*]).

Les requêtes avec les chemins racine [!DNL /is-catalog] et [!DNL /is/cache] doivent toujours être exclues de toute analyse du trafic client.
