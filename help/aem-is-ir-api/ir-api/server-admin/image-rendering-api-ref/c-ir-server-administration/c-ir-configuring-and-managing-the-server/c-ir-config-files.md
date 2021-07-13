---
description: Les paramètres de configuration du rendu d’image sont stockés dans le fichier de configuration du serveur Platform.
solution: Experience Manager
title: Fichiers de configuration
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: 44ffebae-4933-455b-a902-4f6e7bb69184
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# Fichiers de configuration{#configuration-files}

Les paramètres de configuration du rendu d’image sont stockés dans le fichier de configuration du serveur Platform.

Le fichier de configuration du serveur Platform se trouve à l’emplacement suivant : [!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]. Ce fichier est un fichier de propriétés JAVA. Il faut veiller à respecter les conventions appropriées, sinon le serveur Platform risque de ne pas démarrer. Une double barre oblique inverse (`\\`) ou une seule barre oblique inverse (/) doit être utilisée à la place d’une simple barre oblique inverse (\) dans les chemins d’accès aux fichiers Windows, car la barre oblique inverse est utilisée comme caractère d’échappement dans ce type de fichier. Le fichier contient des propriétés non documentées, qui sont destinées à un usage interne du serveur et ne doivent pas être modifiées.

Reportez-vous à la [Référence des paramètres de configuration](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81) pour obtenir la liste de tous les paramètres de configuration de rendu d’image.
