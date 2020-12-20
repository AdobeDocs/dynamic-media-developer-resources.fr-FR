---
description: Les paramètres de configuration du rendu d’image sont stockés dans le fichier de configuration du serveur de plateformes.
seo-description: Les paramètres de configuration du rendu d’image sont stockés dans le fichier de configuration du serveur de plateformes.
seo-title: Fichiers de configuration
solution: Experience Manager
title: Fichiers de configuration
topic: Scene7 Image Serving - Image Rendering API
uuid: ffd1c65b-e084-4a7e-9a15-600d6c5b173a
translation-type: tm+mt
source-git-commit: a47f2b4ef8ebef0c8218dafa4678443aa61241f5
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---


# Fichiers de configuration{#configuration-files}

Les paramètres de configuration du rendu d’image sont stockés dans le fichier de configuration du serveur de plateformes.

Le fichier de configuration du serveur de plate-forme se trouve à l&#39;adresse [ ! DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]. Ce fichier est un fichier de propriétés JAVA. Il faut prendre soin de respecter les conventions appropriées, sinon le serveur de plateformes risque de ne pas être en début. Une barre oblique inverse de doublon (`\\`) ou une seule barre oblique (/) doit être utilisée à la place d&#39;une simple barre oblique inverse (\) dans les chemins d&#39;accès aux fichiers Windows, car la barre oblique inverse est utilisée comme caractère d&#39;échappement dans ce type de fichier. Le fichier contient des propriétés non documentées qui sont destinées à un serveur interne et ne doivent pas être modifiées.

Consultez la [Référence des paramètres de configuration](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81) pour une liste de tous les paramètres de configuration de rendu d’image.
