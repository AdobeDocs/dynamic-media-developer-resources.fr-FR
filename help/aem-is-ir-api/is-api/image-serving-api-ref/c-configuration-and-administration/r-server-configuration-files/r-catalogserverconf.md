---
description: Contient les paramètres liés à la gestion des catalogues d’images.
seo-description: Contient les paramètres liés à la gestion des catalogues d’images.
seo-title: catalog-server.conf
solution: Experience Manager
title: catalog-server.conf
topic: Scene7 Image Serving - Image Rendering API
uuid: 797a43d2-18f5-4735-8b19-da231952b1a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---


# catalog-server.conf{#catalog-server-conf}

Contient les paramètres liés à la gestion des catalogues d’images.

Ce fichier est un fichier de propriétés JAVA. Il faut veiller à respecter les conventions appropriées ; dans le cas contraire, le serveur de plateformes risque de ne pas être en début. Utilisez une barre oblique inverse de doublon &quot;\\&quot; ou une barre oblique inverse &quot;/&quot; au lieu d&#39;une barre oblique inverse &quot;\&quot; dans les chemins d&#39;accès aux fichiers Windows. La barre oblique inverse est utilisée comme caractère d’échappement dans ce type de fichier.

Les modifications apportées à ce fichier prennent effet peu de temps après leur enregistrement.

Seuls les paramètres répertoriés ci-dessous peuvent être modifiés dans [!DNL catalog-service.conf]. Si un paramètre particulier est absent, il peut être ajouté n’importe où dans le fichier. Une seule instance de chaque paramètre peut être présente.

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`
