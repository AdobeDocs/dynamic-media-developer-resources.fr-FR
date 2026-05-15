---
title: Réponses des visionneuses de médias
description: Les paramètres de cette section s’appliquent aux réponses de visionneuse de médias obtenues par le modificateur req=set.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e3833726-d345-4741-8096-d74f299ac9fc
TQID: 'https://experienceleague.adobe.com/FNUguOqf8f5FnIeGTzheZU-8zCXqwRMU3YGyvYDA0uM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 147
ht-degree: 0%

---

# Réponses des visionneuses de médias{#media-set-responses}

Les paramètres de cette section s’appliquent aux réponses de visionneuse de médias obtenues par le modificateur `req=set`.

## PS::fvctx.useCatalogRecordValidation - Politique de mise en cache {#section-9accb087d16548a988993bb30395a6f6}

Cette propriété contrôle la politique de mise en cache lorsque vous déterminez si une réponse définie récupérée à partir d’un cache doit être régénérée. Si la propriété est désactivée, l’horodatage du fichier [!DNL catalog.ini] est utilisé pour la validation. Si la propriété est activée, la date et l’heure `catalog::LastModified` les plus récentes de tous les enregistrements référencés sont utilisées pour la validation.

## PS::fvctx.nestedLimit - Limite d’imbrication {#section-280210341f1647fea02590e7069934d2}

Profondeur d’imbrication maximale de toute réponse `req=set`. Si cette profondeur est dépassée, une erreur est renvoyée.

## PS::fvctx.brochureLimit - Limite de la brochure {#section-fe36e47db49244cea7f07e9dd3639440}

Nombre maximal de brochures de catalogue électronique dans la réponse `req=set` qui contient toutes les métadonnées associées. Une fois cette limite dépassée, tous les mappages privés et les données utilisateur associés à l’élément de brochure sont supprimés.
