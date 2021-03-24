---
description: Détermine si un lot de fichiers est prêt à être publié.
solution: Experience Manager
title: setAssetsPublishState
feature: Dynamic Media Classic, SDK/API, Gestion des ressources
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 11%

---


# setAssetsPublishState{#setassetspublishstate}

Détermine si un lot de fichiers est prêt à être publié.

Il s’agit de la version par lot de [setAssetState](../../../operations/c-operations-intro/c-methods/r-set-asset-publish-state.md#reference-9efc2eeea42348e0b1d5f3d1005c6563).

## Types d’utilisateur autorisés {#section-0804726f683944dbbe9acfc3d35ccf25}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L’utilisateur doit disposer d’un accès en lecture et en écriture à la ressource.

## Paramètres {#section-3e49d7859f8647b990d75373cc8dbc24}

**Entrée (setAssetsPublishStateParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée de société. |
| `*`publishStateUpdateArray`*` | `types:PublishStateUpdateArray` | Oui | Tableau des valeurs d’état de publication pour les ressources. |

**Output (setAssetsPublishStateParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Oui | Nombre de ressources mises à jour avec succès. |
| `*`warningCount`*` | `xsd:int` | Oui | Nombre de fichiers qui ont généré un avertissement lorsque l’opération tentait de les mettre à jour. |
| `*`errorCount`*` | `xsd:int` | Oui | Nombre de fichiers qui ont généré une erreur lorsque l’opération a tenté de les supprimer. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | Non | Détails associés aux mises à jour de la ressource qui ont généré un avertissement. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | Non | Détails associés aux mises à jour de la ressource qui ont généré une erreur. |

## Exemples {#section-38cfdd3436214a06a1bae16875501d51}

Cet exemple de code définit l&#39;état de publication d&#39;un fichier.

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

