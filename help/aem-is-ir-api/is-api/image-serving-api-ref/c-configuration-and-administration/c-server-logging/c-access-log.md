---
description: Il s’agit du journal principal qui effectue le suivi de toutes les requêtes HTTP envoyées au serveur de plateformes. Le rendu d’image, s’il est activé, écrit ses données du journal d’accès dans le même fichier.
seo-description: Il s’agit du journal principal qui effectue le suivi de toutes les requêtes HTTP envoyées au serveur de plateformes. Le rendu d’image, s’il est activé, écrit ses données du journal d’accès dans le même fichier.
seo-title: Journal d’accès
solution: Experience Manager
title: Journal d’accès
topic: Scene7 Image Serving - Image Rendering API
uuid: 33cd4338-1fe7-46ac-83f5-200ea26f1e22
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Journal d’accès{#access-log}

Il s’agit du journal principal qui effectue le suivi de toutes les requêtes HTTP envoyées au serveur de plateformes. Le rendu d’image, s’il est activé, écrit ses données du journal d’accès dans le même fichier.

Le journal d’accès est configuré dans server.xml.

>[!NOTE] {class=&quot;- rubrique/note &quot;}
>
>Outre le trafic client pour la diffusion d’images ( [!DNL /is/image/*]) et le rendu d’images ( [!DNL /ir/render/*]), le journal d’accès peut inclure un certain trafic interne : l’accès au système de catalogue du serveur de plateformes ( [!DNL /is-catalog/*]), le partage du cache et les demandes de redirection d’erreur ( [!DNL /is/cache/*]), l’accès aux autres packs déployés sur le serveur de plateformes, tels que les visionneuses Scene7 ( [!DNL /is-viewers/*]), les demandes de trafic statique et de contenu statique traitées par le serveur de plateformes (p. ex. [!DNL /is-docs/*]).

Les requêtes avec [!DNL /is-catalog] et [!DNL /is/cache] chemins racine doivent toujours être exclues de tout trafic client  .
