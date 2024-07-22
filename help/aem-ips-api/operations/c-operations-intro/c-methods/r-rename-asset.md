---
description: Renomme une ressource.
solution: Experience Manager
title: renameAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f3fff3c1-1b48-4d86-8a81-f75be00fc329
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 6%

---

# renameAsset{#renameasset}

Renomme une ressource.

>[!NOTE]
>
>Le paramètre `renameFiles` a été abandonné pour les versions antérieures et supprimé de `renameAsset`. Le chemin d’accès au fichier virtuel est modifié pour correspondre au nouveau nom de la ressource (en conservant l’extension du fichier), tandis que les chemins d’accès aux fichiers physiques ne sont pas affectés. Les clients API doivent supprimer les références à ce paramètre lors de la mise à jour vers la nouvelle version de l’API.

## Types d’utilisateurs autorisés {#section-cc27ad713c6d498b8f056850b20976f4}

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
| companyHandle | `xsd:string` | Oui | Gestionnaire de la société à laquelle appartient la ressource. |
| assetHandle | `xsd:string` | Oui | Gestionnaire de la ressource à renommer. |
| newName | `xsd:string` | Oui | Nouveau nom de la ressource. |
| validateName | `xsd:boolean` | Oui | Si le `validateName` est `true` et que le type de ressource nécessite un identifiant IPS unique, le nouveau nom est analysé pour l’unicité globale et `renameAsset` renvoie une erreur s’il n’est pas unique. |

**Sortie (renameAssetReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération. Voir la description de l’élément `<ns1:validateName>` pour obtenir des avertissements sur cet élément.

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
