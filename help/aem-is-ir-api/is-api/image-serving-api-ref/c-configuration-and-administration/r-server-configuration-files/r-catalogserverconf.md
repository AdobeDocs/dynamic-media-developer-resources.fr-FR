---
description: Contient les paramètres relatifs à la gestion des catalogues d’images.
solution: Experience Manager
title: catalog-server.conf
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 55e55381-3828-4937-8746-a74e82d6ca38
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 0%

---

# catalog-server.conf{#catalog-server-conf}

Contient les paramètres relatifs à la gestion des catalogues d’images.

Ce fichier est un fichier de propriétés JAVA. Il faut veiller à respecter les conventions appropriées ; dans le cas contraire, [!DNL Platform Server] peut ne pas démarrer. Utilisez une double barre oblique inverse &quot;\\&quot; ou une seule barre oblique inverse &quot;/&quot; au lieu d’une barre oblique inverse &quot;\&quot; dans les chemins d’accès aux fichiers Windows. La barre oblique inverse est utilisée comme caractère d’échappement dans ce type de fichier.

Les modifications apportées à ce fichier prennent effet peu de temps après l’enregistrement du fichier.

Seuls les paramètres répertoriés ci-dessous peuvent être modifiés dans [!DNL catalog-service.conf]. Si un paramètre particulier est absent, il peut être ajouté n’importe où dans le fichier . Une seule instance de chaque paramètre peut être présente.

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`
