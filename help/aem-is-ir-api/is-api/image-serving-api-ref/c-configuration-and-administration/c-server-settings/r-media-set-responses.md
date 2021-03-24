---
description: Les paramètres de cette section s’appliquent aux réponses de visionneuse de supports obtenues par le modificateur req=set.
solution: Experience Manager
title: Réponses des visionneuses de supports
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '155'
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
