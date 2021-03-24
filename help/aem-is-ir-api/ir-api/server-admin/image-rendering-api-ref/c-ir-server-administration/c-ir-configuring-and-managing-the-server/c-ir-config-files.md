---
description: Les paramètres de configuration du rendu d’image sont stockés dans le fichier de configuration du serveur de plateformes.
solution: Experience Manager
title: Fichiers de configuration
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---


# Fichiers de configuration{#configuration-files}

Les paramètres de configuration du rendu d’image sont stockés dans le fichier de configuration du serveur de plateformes.

Le fichier de configuration du serveur de plate-forme se trouve à l&#39;adresse [ ! DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]. Ce fichier est un fichier de propriétés JAVA. Il faut prendre soin de respecter les conventions appropriées, sinon le serveur de plateformes risque de ne pas être en début. Une barre oblique inverse de doublon (`\\`) ou une seule barre oblique (/) doit être utilisée à la place d&#39;une simple barre oblique inverse (\) dans les chemins d&#39;accès aux fichiers Windows, car la barre oblique inverse est utilisée comme caractère d&#39;échappement dans ce type de fichier. Le fichier contient des propriétés non documentées qui sont destinées à un serveur interne et ne doivent pas être modifiées.

Consultez la [Référence des paramètres de configuration](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81) pour une liste de tous les paramètres de configuration de rendu d’image.
