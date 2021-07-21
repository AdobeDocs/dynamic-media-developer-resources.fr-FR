---
description: Supprime une ressource.
solution: Experience Manager
title: deleteAsset
feature: Dynamic Media Classic,SDK/API,Gestion des ressources
role: Developer,Admin
exl-id: dacea36e-3d40-4aaf-94fd-f0709830caf9
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 12%

---

# deleteAsset{#deleteasset}

Supprime une ressource.

Syntaxe

## Types d’utilisateurs autorisés {#section-e913be43b684491daf02bc73211e4290}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L’utilisateur doit disposer d’un accès en lecture et en suppression à la ressource.

## Paramètres {#section-0eed164e278b456fbdfb7a50727a0416}

**Entrée (deleteAssetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Gestionnaire de la société à laquelle appartient le dossier. |
| `*`assetHandle`*` | `xsd:string` | Oui | Gestionnaire de la ressource à supprimer. |

**Sortie (deleteAssetParam)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-d5657289f5234bb0a613dcf691507958}

Cet exemple de code supprime tout type de ressource d’une société spécifique. Elle nécessite un gestionnaire de ressources, que vous devez obtenir d’une autre opération.

**Request**

```java
<ns1:deleteAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
</ns1:deleteAssetParam>
```

**Réponse**

Aucune
