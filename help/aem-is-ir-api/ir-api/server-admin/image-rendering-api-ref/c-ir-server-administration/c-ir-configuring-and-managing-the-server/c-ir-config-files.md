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

---


# Fichiers de configuration{#configuration-files}

Les paramètres de configuration du rendu d’image sont stockés dans le fichier de configuration du serveur de plateformes.

Le fichier de configuration du serveur de plateformes se trouve à l’emplacement suivant : [!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]. Ce fichier est un fichier de propriétés JAVA. Veillez à respecter les conventions appropriées, sinon le serveur de plateformes risque de ne pas . Une barre oblique inverse (`\\`) ou une seule barre oblique (/) doit être utilisée à la place d’une simple barre oblique inverse (\) dans les chemins d’accès aux fichiers Windows, car la barre oblique inverse est utilisée comme caractère d’échappement dans ce type de fichier. Le fichier contient des propriétés non documentées, qui sont destinées à un usage interne du serveur et ne doivent pas être modifiées.

Reportez-vous à la référence [des paramètres de](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81) configuration pour obtenir un de tous les paramètres de configuration du rendu d’image.
