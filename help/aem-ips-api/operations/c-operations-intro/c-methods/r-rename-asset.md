---
description: Renomme un fichier.
solution: Experience Manager
title: renameAsset
feature: Dynamic Media Classic, SDK/API, Gestion des ressources
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 7%

---


# renameAsset{#renameasset}

Renomme un fichier.

>[!NOTE]
>
>Le paramètre `renameFiles` a été abandonné pour les versions antérieures et supprimé de `renameAsset`. Le chemin d’accès au fichier virtuel est modifié pour correspondre au nouveau nom de fichier (en conservant l’extension de fichier), tandis que les chemins d’accès aux fichiers physiques ne sont pas affectés. Les clients d’API doivent supprimer les références à ce paramètre lors de la mise à jour vers la nouvelle version de l’API.

## Types d’utilisateur autorisés {#section-cc27ad713c6d498b8f056850b20976f4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImpagePortalContribUser`

>[!NOTE]
>
>L’utilisateur doit disposer d’un accès en lecture et en écriture à la ressource.

## Paramètres {#section-ef95a994106841e0ab346dd4cf672258}

**Entrée (renameAssetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée de la société à laquelle appartient le fichier. |
| `*`assetHandle`*` | `xsd:string` | Oui | Identifiant de la ressource que vous souhaitez renommer. |
| `*`newName`*` | `xsd:string` | Oui | Nouveau nom du fichier. |
| `*`validateName`*` | `xsd:boolean` | Oui | Si `validateName` est `true` et que le type de ressource nécessite un identifiant IPS unique, le nouveau nom est vérifié pour l&#39;unicité globale et `renameAsset` renvoie une erreur s&#39;il n&#39;est pas unique. |

**Sortie (renameAssetReturn)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération. Voir la description de l’élément `<ns1:validateName>` pour obtenir des mises en garde sur cet élément.

## Exemples {#section-a0ddffd62bec42e09069f22ceb486f8a}

Cet exemple de code renomme un fichier

**Request**

```java
<ns1:renameAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
   <ns1:newName>My Newly Renamed Image</ns1:newName>
   <ns1:validateName>true</ns1:validateName>
   <ns1:renameFiles>true</ns1:renameFiles>
</ns1:renameAssetParam>
```

**Réponse**

Aucune
