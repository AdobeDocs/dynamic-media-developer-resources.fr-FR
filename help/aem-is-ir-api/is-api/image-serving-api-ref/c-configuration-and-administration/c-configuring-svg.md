---
description: Le composant SvgRender est une application Java indépendante.
solution: Experience Manager
title: Configuration du format SVG
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9013e13f-818f-41b4-80b6-2615d9a8742f
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 3%

---

# Configuration du format SVG{#configuring-svg}

Le composant SvgRender est une application Java indépendante.

Les paramètres de configuration SVG se trouvent dans [!DNL PlatformServer.conf], [!DNL SVG.conf], [!DNL ImageServerRegistry.xml]et [!DNL ServerSupervisorRegistry.xml].

Une connexion socket est utilisée pour communiquer entre SvgRender et Image Server. Le numéro de port est 27346. Si nécessaire, il est possible de la modifier en la définissant `SVGRender.port` sur [!DNL svg.conf] `<SVGTcpPort>` [!DNL ImageServerRegistry.xml] une nouvelle valeur.

## Voir aussi {#section-c085b47d54d44059bdaa67fd5e226e91}

[Paramètres de configuration SVG](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
