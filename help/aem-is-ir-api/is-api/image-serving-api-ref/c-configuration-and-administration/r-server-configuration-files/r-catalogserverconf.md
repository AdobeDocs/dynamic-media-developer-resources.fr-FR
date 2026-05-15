---
description: Contient les paramètres liés à la gestion des catalogues d’images.
solution: Experience Manager
title: catalog-server.conf
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 55e55381-3828-4937-8746-a74e82d6ca38
TQID: 'https://experienceleague.adobe.com/GdtVY3WMO9F6C5vzkOHdVoMW-f6-L1cJGUt1KUCvLJ8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 113
ht-degree: 0%

---

# catalog-server.conf{#catalog-server-conf}

Contient les paramètres liés à la gestion des catalogues d’images.

Ce fichier est un fichier de propriétés JAVA. Il faut veiller à respecter les conventions appropriées, faute de quoi la [!DNL Platform Server] risque de ne pas démarrer. Utilisez une double barre oblique inverse &#39;\\&#39; ou une seule barre oblique inverse &#39;/&#39; au lieu d’une barre oblique inverse &#39;\&#39; dans les chemins d’accès aux fichiers Windows. La barre oblique inverse est utilisée comme caractère d’échappement dans ce type de fichier.

Les modifications apportées à ce fichier prennent effet peu de temps après son enregistrement.

Seuls les paramètres répertoriés ci-dessous peuvent être modifiés dans [!DNL catalog-service.conf]. Si un paramètre particulier est absent, il peut être ajouté n’importe où dans le fichier. Une seule instance de chaque paramètre peut être présente.

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`
