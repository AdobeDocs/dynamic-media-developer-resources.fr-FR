---
description: Détermine si un lot de fichiers est prêt à être publié.
seo-description: Détermine si un lot de fichiers est prêt à être publié.
seo-title: setAssetsPublishState
solution: Experience Manager
title: setAssetsPublishState
topic: Scene7 Image Production System API
uuid: 2910cd6c-573b-405c-864d-a0136ac5472d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAssetsPublishState{#setassetspublishstate}

Détermine si un lot de fichiers est prêt à être publié.

Il s’agit de la version par lot de [setAssetState](../../../operations/c-operations-intro/c-methods/r-set-asset-publish-state.md#reference-9efc2eeea42348e0b1d5f3d1005c6563).

## Types d’utilisateurs autorisés {#section-0804726f683944dbbe9acfc3d35ccf25}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L’utilisateur doit disposer d’un accès en lecture et en écriture au fichier.

## Paramètres {#section-3e49d7859f8647b990d75373cc8dbc24}

**Input (setAssetsPublishStateParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui |  poignée. |
| ` *`publishStateUpdateArray`*` | `types:PublishStateUpdateArray` | Oui | Tableau des valeurs d’état de publication pour les ressources. |

**Output (setAssetsPublishStateParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Oui | Nombre de fichiers mis à jour. |
| ` *`warningCount`*` | `xsd:int` | Oui | Nombre de fichiers qui ont généré un avertissement lorsque l’opération tentait de les mettre à jour. |
| ` *`errorCount`*` | `xsd:int` | Oui | Nombre de fichiers qui ont généré une erreur lorsque l’opération tentait de les supprimer. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | Non | Détails associés aux mises à jour de ressources qui ont généré un avertissement. |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | Non | Détails associés aux mises à jour de ressources qui ont généré une erreur. |

## Exemples {#section-38cfdd3436214a06a1bae16875501d51}

Cet exemple de code définit l’état de publication d’un fichier.

**Request**

```java
<element name="setAssetsPublishStateParam">
   <complexType>
      <sequence>
         <element name="companyHandle" type="xsd:string"/>
         <element name="publishStateUpdateArray" type="types:PublishStateUpdateArray"/>
      </sequence>
   </complexType>
</element>
```

**Réponse**

```java
<element name="setAssetsPublishStateReturn">
   <complexType>
      <sequence>
         <element name="successCount" type="xsd:int"/>
         <element name="warningCount" type="xsd:int"/>
         <element name="errorCount" type="xsd:int"/>
         <element name="warningDetailArray"type="types:AssetOperationFaultArray" minOccurs="0"/>
         <element name="errorDetailArray"type="types:AssetOperationFaultArray" minOccurs="0"/>
      </sequence>
   </complexType>
</element>
```

