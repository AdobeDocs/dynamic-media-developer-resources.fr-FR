---
title: Réponses de visionneuse de médias
description: Les paramètres de cette section s’appliquent aux réponses de visionneuse de médias obtenues par le modificateur req=set .
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e3833726-d345-4741-8096-d74f299ac9fc
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# Réponses de visionneuse de médias{#media-set-responses}

Les paramètres de cette section s’appliquent aux réponses de visionneuse de médias obtenues par le modificateur `req=set`.

## PS::fvctx.useCatalogRecordValidation - Stratégie de mise en cache {#section-9accb087d16548a988993bb30395a6f6}

Cette propriété contrôle la stratégie de mise en cache lorsque vous déterminez si une réponse définie récupérée à partir d’un cache doit être régénérée. Si la propriété est désactivée, l’horodatage du fichier [!DNL catalog.ini] est utilisé pour la validation. Si la propriété est activée, le dernier horodatage `catalog::LastModified` de tous les enregistrements référencés est utilisé pour la validation.

## PS::fvctx.nestingLimit - Limite d’imbrication {#section-280210341f1647fea02590e7069934d2}

Profondeur d’imbrication maximale de toute réponse `req=set`. Si cette profondeur est dépassée, une erreur est renvoyée.

## PS::fvctx.brochureLimit - Limite de navigation {#section-fe36e47db49244cea7f07e9dd3639440}

Nombre maximum de brochures de catalogue électronique dans la réponse `req=set` qui contient toutes les métadonnées associées. Une fois cette limite dépassée, toutes les cartes privées et les données utilisateur associées à l’élément de brochure sont supprimées.
