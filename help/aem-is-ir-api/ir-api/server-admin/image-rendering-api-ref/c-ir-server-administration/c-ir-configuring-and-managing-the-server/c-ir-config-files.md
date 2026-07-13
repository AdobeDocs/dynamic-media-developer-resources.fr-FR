---
description: Les paramètres de configuration du rendu d’image sont stockés dans le fichier  [!DNL Platform Server]  configuration .
solution: Experience Manager
title: Fichiers de configuration
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 44ffebae-4933-455b-a902-4f6e7bb69184
TQID: 'https://experienceleague.adobe.com/KTBXtuSOstPMi7bPQg70jyUVCqcXlLiLPiFFhyp9iFg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 122
ht-degree: 0%

---

# Fichiers de configuration{#configuration-files}

Les paramètres de configuration du rendu d’image sont stockés dans le fichier de configuration de [!DNL Platform Server].

Le fichier de configuration du serveur Platform se trouve à l’emplacement suivant : [!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]. Ce fichier est un fichier de propriétés JAVA. Veillez à respecter les conventions appropriées, sinon le [!DNL Platform Server] risque de ne pas démarrer. Une double barre oblique inverse (`\\`) ou une simple barre oblique inverse (/) doit être utilisée au lieu d’une simple barre oblique inverse (\) dans les chemins d’accès aux fichiers Windows, car la barre oblique inverse est utilisée comme caractère d’échappement dans ce type de fichier. Le fichier contient des propriétés non documentées, qui sont destinées à une utilisation interne au serveur et ne doivent pas être modifiées.

Pour obtenir la liste de tous les paramètres de configuration de rendu d’image](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81) reportez-vous à la [ Référence des paramètres de configuration .

