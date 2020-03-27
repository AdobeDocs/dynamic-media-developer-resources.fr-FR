---
description: Le composant SvgRender est une application Java indépendante.
seo-description: Le composant SvgRender est une application Java indépendante.
seo-title: Configuration de SVG
solution: Experience Manager
title: Configuration de SVG
topic: Scene7 Image Serving - Image Rendering API
uuid: f6e131af-283e-4649-b349-123489c0838d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Configuration de SVG{#configuring-svg}

Le composant SvgRender est une application Java indépendante.

Les paramètres de configuration SVG se trouvent dans [!DNL PlatformServer.conf], [!DNL SVG.conf], [!DNL ImageServerRegistry.xml]et [!DNL ServerSupervisorRegistry.xml].

Une connexion socket est utilisée pour communiquer entre SvgRender et Image Server. Le numéro de port est 27346. Si nécessaire, vous pouvez le modifier en définissant `SVGRender.port` dans [!DNL svg.conf] et `<SVGTcpPort>` dans [!DNL ImageServerRegistry.xml] une nouvelle valeur.

## Voir aussi {#section-c085b47d54d44059bdaa67fd5e226e91}

[Paramètres de configuration SVG](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
