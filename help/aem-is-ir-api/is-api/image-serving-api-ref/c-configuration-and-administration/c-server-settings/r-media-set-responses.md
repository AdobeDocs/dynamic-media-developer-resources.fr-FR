---
description: Les paramètres de cette section s’appliquent aux réponses de visionneuse de médias obtenues par le modificateur req=set .
solution: Experience Manager
title: Réponses de visionneuse de médias
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: e3833726-d345-4741-8096-d74f299ac9fc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---

# Réponses de visionneuse de médias{#media-set-responses}

Les paramètres de cette section s’appliquent aux réponses de visionneuse de médias obtenues par le modificateur req=set .

## PS::fvctx.useCatalogRecordValidation - Stratégie de mise en cache {#section-9accb087d16548a988993bb30395a6f6}

Cette propriété contrôle la stratégie de mise en cache lorsque vous déterminez si la réponse définie récupérée à partir du cache doit être recréée. Si la propriété est désactivée, l’horodatage du fichier [!DNL catalog.ini] est utilisé pour la validation. Si la propriété est activée, l’horodatage `catalog::LastModified` le plus récent de tous les enregistrements référencés est utilisé pour la validation.

## PS::fvctx.nestingLimit - Limite d’imbrication {#section-280210341f1647fea02590e7069934d2}

Profondeur d’imbrication maximale de toute réponse `req=set`. Si cette profondeur est dépassée, une erreur est renvoyée.

## PS::fvctx.brochureLimit - Limite de navigation {#section-fe36e47db49244cea7f07e9dd3639440}

Nombre maximum de brochures de catalogue électronique dans la réponse `req=set` contenant toutes les métadonnées associées. Une fois cette limite dépassée, toutes les cartes privées et les données utilisateur associées à l’élément de brochure sont supprimées.
