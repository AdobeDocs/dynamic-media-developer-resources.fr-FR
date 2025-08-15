---
title: Réponses des visionneuses de médias
description: Les paramètres de cette section s’appliquent aux réponses de la visionneuse de médias obtenues par le modificateur req=set.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e3833726-d345-4741-8096-d74f299ac9fc
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# Réponses des visionneuses de médias{#media-set-responses}

Les paramètres de cette section s’appliquent aux réponses de la visionneuse de médias obtenues par le `req=set` modificateur.

## PS ::fvctx.useCatalogRecordValidation - Stratégie de mise en cache {#section-9accb087d16548a988993bb30395a6f6}

Cette propriété contrôle la stratégie de mise en cache lorsqu’elle détermine si une réponse définie récupérée à partir d’un cache doit être régénérée. Si la propriété est désactivée, l’horodatage du fichier est utilisé pour la [!DNL catalog.ini] validation. Si la propriété est activée, le dernier `catalog::LastModified` horodatage de tous les enregistrements référencés est utilisé pour la validation.

## PS ::fvctx.nestingLimit - Limite d’imbrication {#section-280210341f1647fea02590e7069934d2}

Profondeur maximale d’imbrication de n’importe quelle `req=set` réponse. Si cette profondeur est dépassée, une erreur est renvoyée.

## PS ::fvctx.brochureLimit - Limite brochure {#section-fe36e47db49244cea7f07e9dd3639440}

Nombre maximal de brochures de catalogue électronique dans la `req=set` réponse qui contient toutes les métadonnées associées. Une fois cette limite dépassée, toutes les cartes privées et les données utilisateur associées à l’élément de brochure sont supprimées.
