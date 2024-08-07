---
description: Les paramètres de configuration du rendu d’image sont stockés dans le fichier de configuration  [!DNL Platform Server] .
solution: Experience Manager
title: Fichiers de configuration
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 44ffebae-4933-455b-a902-4f6e7bb69184
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# Fichiers de configuration{#configuration-files}

Les paramètres de configuration du rendu d’image sont stockés dans le fichier de configuration [!DNL Platform Server].

Le fichier de configuration du serveur de plateforme se trouve à l’adresse [!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]. Ce fichier est un fichier de propriétés JAVA. Il faut veiller à respecter les conventions appropriées, sinon [!DNL Platform Server] risque de ne pas démarrer. Une double barre oblique inverse (`\\`) ou une seule barre oblique inverse (/) doit être utilisée à la place d’une simple barre oblique inverse (\) dans les chemins d’accès aux fichiers Windows, car la barre oblique inverse est utilisée comme caractère d’échappement dans ce type de fichier. Le fichier contient des propriétés non documentées, qui sont destinées à un usage interne du serveur et ne doivent pas être modifiées.

Pour obtenir la liste de tous les paramètres de configuration de rendu d’image, reportez-vous à la [référence des paramètres de configuration](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81).
