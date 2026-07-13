---
description: Renomme une ressource.
solution: Experience Manager
title: renameAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f3fff3c1-1b48-4d86-8a81-f75be00fc329
TQID: 'https://experienceleague.adobe.com/m1AT0yP7u3PFZCs8uoFQxQoGNtfJe49vzGt8e3wTx8s'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 173
ht-degree: 6%

---

# renameAsset{#renameasset}

Renomme une ressource.

>[!NOTE]
>
>Le paramètre `renameFiles` a été abandonné pour les versions antérieures et supprimé de `renameAsset`. Le chemin d’accès au fichier virtuel est modifié pour correspondre au nouveau nom de ressource (en préservant l’extension de fichier), tandis que les chemins d’accès aux fichiers physiques ne sont pas affectés. Les clients d’API doivent supprimer les références à ce paramètre lors de la mise à jour vers la nouvelle version de l’API.

## Types d’utilisateurs autorisés {#section-cc27ad713c6d498b8f056850b20976f4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImpagePortalContribUser`

>[!NOTE]
>
>L’utilisateur doit disposer d’un accès en lecture et écriture à la ressource.

## Paramètres {#section-ef95a994106841e0ab346dd4cf672258}

**Input (renameAssetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Identifiant de la société à laquelle appartient la ressource. |
| assetHandle | `xsd:string` | Oui | La poignée de la ressource à renommer. |
| newName | `xsd:string` | Oui | Nouveau nom de la ressource. |
| validateName | `xsd:boolean` | Oui | Si le `validateName` est `true` et que le type de ressource nécessite un identifiant IPS unique, le nouveau nom est vérifié pour l’unicité globale et `renameAsset` génère une erreur s’il n’est pas unique. |

**Output (renameAssetReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération. Consultez la description de l’élément `<ns1:validateName>` pour obtenir des informations sur cet élément.

## Exemples {#section-a0ddffd62bec42e09069f22ceb486f8a}

Cet exemple de code renomme une ressource

**Requête**

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

