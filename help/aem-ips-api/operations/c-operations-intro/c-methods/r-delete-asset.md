---
description: Supprime un fichier.
seo-description: Supprime un fichier.
seo-title: deleteAsset
solution: Experience Manager
title: deleteAsset
uuid: 47f700e0-04bf-4d33-a18a-d938f7e9e326
feature: Dynamic Media Classic, SDK/API, Gestion des ressources
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 11%

---


# deleteAsset{#deleteasset}

Supprime un fichier.

Syntaxe

## Types d’utilisateur autorisés {#section-e913be43b684491daf02bc73211e4290}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L’utilisateur doit avoir accès en lecture et en suppression à la ressource.

## Paramètres {#section-0eed164e278b456fbdfb7a50727a0416}

**Entrée (deleteAssetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Identifiant de la société à laquelle appartient le dossier. |
| `*`assetHandle`*` | `xsd:string` | Oui | Poignée du fichier à supprimer. |

**Output (deleteAssetParam)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-d5657289f5234bb0a613dcf691507958}

Cet exemple de code supprime tout type de fichier d&#39;une société spécifique. Elle nécessite un gestionnaire de ressources, que vous devez obtenir d’une autre opération.

**Request**

```java
<ns1:deleteAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
</ns1:deleteAssetParam>
```

**Réponse**

Aucune
