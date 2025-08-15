---
description: Détermine si un lot de ressources est prêt à être publié.
solution: Experience Manager
title: setAssetsPublishState
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: dce324e4-cf86-4a65-ab00-8cd2bba20f8f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 11%

---

# setAssetsPublishState{#setassetspublishstate}

Détermine si un lot de ressources est prêt à être publié.

Il s’agit de la version par lots de [setAssetState](../../../operations/c-operations-intro/c-methods/r-set-asset-publish-state.md#reference-9efc2eeea42348e0b1d5f3d1005c6563).

## Types d’utilisateurs autorisés {#section-0804726f683944dbbe9acfc3d35ccf25}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L’utilisateur doit disposer d’un accès en lecture et en écriture à l’actif.

## Paramètres {#section-3e49d7859f8647b990d75373cc8dbc24}

**Input (setAssetsPublishStateParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| CompanyHandle | `xsd:string` | Oui | Pseudo de l’entreprise. |
| publishStateUpdateArray | `types:PublishStateUpdateArray` | Oui | Tableau des valeurs d’état de publication des ressources. |

**Output (setAssetsPublishStateParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| Compte de succès | `xsd:int` | Oui | Nombre de ressources mises à jour réussies. |
| Nombre d’avertissements | `xsd:int` | Oui | Nombre d’actifs qui ont généré un avertissement lorsque l’opération a tenté de les mettre à jour. |
| Nombre d’erreurs | `xsd:int` | Oui | Nombre d’actifs qui ont généré une erreur lorsque l’opération a tenté de les supprimer. |
| Tableau des détails de l’avertissement | `types:AssetOperationFaultArray` | Non | Les détails associés aux mises à jour des ressources qui ont généré un avertissement. |
| Tableau errorDetailArray | `types:AssetOperationFaultArray` | Non | Les détails associés aux mises à jour de ressources qui ont généré une erreur. |

## Exemples {#section-38cfdd3436214a06a1bae16875501d51}

Cet exemple de code définit l’état de publication d’une ressource.

**Demander**

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
