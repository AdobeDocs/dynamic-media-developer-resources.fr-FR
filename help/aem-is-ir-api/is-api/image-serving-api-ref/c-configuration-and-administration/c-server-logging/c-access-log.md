---
description: Il s'agit du Principal journal qui suit toutes les requêtes HTTP envoyées au serveur de plateformes. Le rendu d’image, s’il est activé, écrit ses données du journal d’accès dans le même fichier.
seo-description: Il s'agit du Principal journal qui suit toutes les requêtes HTTP envoyées au serveur de plateformes. Le rendu d’image, s’il est activé, écrit ses données du journal d’accès dans le même fichier.
seo-title: Journal d’accès
solution: Experience Manager
title: Journal d’accès
uuid: 33cd4338-1fe7-46ac-83f5-200ea26f1e22
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---


# Journal d&#39;accès{#access-log}

Il s&#39;agit du Principal journal qui suit toutes les requêtes HTTP envoyées au serveur de plateformes. Le rendu d’image, s’il est activé, écrit ses données du journal d’accès dans le même fichier.

Le journal d’accès est configuré dans server.xml.

>[!NOTE]
>
>Outre le trafic client pour la diffusion d’images ( [!DNL /is/image/*]) et le rendu d’images ( [!DNL /ir/render/*]), le journal d’accès peut inclure un certain trafic interne : l&#39;accès au système de catalogue de Platform Server ( [!DNL /is-catalog/*]), le partage du cache et les demandes de redirection d&#39;erreur ( [!DNL /is/cache/*]), l&#39;accès à d&#39;autres packages déployés sur le serveur de plateformes, tels que les visionneuses Dynamic Media ( [!DNL /is-viewers/*]), le trafic statique et les demandes de contenu statique traitées par le serveur de plateformes (par ex. [!DNL /is-docs/*]).

Les requêtes avec des chemins d’accès racine [!DNL /is-catalog] et [!DNL /is/cache] doivent toujours être exclues de toute analyse de trafic client.
