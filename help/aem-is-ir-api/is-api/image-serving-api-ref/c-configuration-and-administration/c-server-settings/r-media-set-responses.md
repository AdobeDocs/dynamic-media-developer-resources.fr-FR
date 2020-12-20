---
description: Les paramètres de cette section s’appliquent aux réponses de visionneuse de supports obtenues par le modificateur req=set.
seo-description: Les paramètres de cette section s’appliquent aux réponses de visionneuse de supports obtenues par le modificateur req=set.
seo-title: Réponses des visionneuses de supports
solution: Experience Manager
title: Réponses des visionneuses de supports
topic: Scene7 Image Serving - Image Rendering API
uuid: 9fa6a38a-cd1f-499b-a2b6-e1a9a6c69ed0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 0%

---


# Réponses des visionneuses de médias{#media-set-responses}

Les paramètres de cette section s’appliquent aux réponses de visionneuse de supports obtenues par le modificateur req=set.

## PS::fvctx.useCatalogRecordValidation - Stratégie de mise en cache {#section-9accb087d16548a988993bb30395a6f6}

Cette propriété contrôle la stratégie de mise en cache lorsque vous déterminez si la réponse définie récupérée du cache doit être régénérée. Si la propriété est désactivée, l’horodatage du fichier [!DNL catalog.ini] est utilisé pour la validation. Si la propriété est activée, l’horodatage `catalog::LastModified` le plus récent de tous les enregistrements référencés est utilisé pour la validation.

## PS::fvctx.nestingLimit - Limite d&#39;imbrication {#section-280210341f1647fea02590e7069934d2}

Profondeur d’imbrication maximale de toute réponse `req=set`. Si cette profondeur est dépassée, une erreur est renvoyée.

## PS::fvctx.brochureLimit - Limite de la brochure {#section-fe36e47db49244cea7f07e9dd3639440}

Nombre maximal de brochures de catalogue électronique dans la réponse `req=set` contenant toutes les métadonnées associées. Une fois cette limite dépassée, toutes les cartes privées et les données utilisateur associées à l’article de la brochure sont supprimées.
