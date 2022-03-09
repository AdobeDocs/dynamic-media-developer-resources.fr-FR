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
ht-degree: 12%

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
>L’utilisateur doit disposer d’un accès en lecture et en écriture à la ressource.

## Paramètres {#section-3e49d7859f8647b990d75373cc8dbc24}

**Entrée (setAssetsPublishStateParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Poignée de la société. |
| publishStateUpdateArray | `types:PublishStateUpdateArray` | Oui | Tableau des valeurs d’état de publication des ressources. |

**Sortie (setAssetsPublishStateParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| successCount | `xsd:int` | Oui | Nombre de ressources mises à jour avec succès. |
| warningCount | `xsd:int` | Oui | Nombre de ressources ayant généré un avertissement lorsque l’opération tentait de les mettre à jour. |
| errorCount | `xsd:int` | Oui | Nombre de ressources qui ont généré une erreur lorsque l’opération a tenté de les supprimer. |
| warningDetailArray | `types:AssetOperationFaultArray` | Non | Détails associés aux mises à jour de la ressource qui ont généré un avertissement. |
| errorDetailArray | `types:AssetOperationFaultArray` | Non | Détails associés aux mises à jour de la ressource qui ont généré une erreur. |

## Exemples {#section-38cfdd3436214a06a1bae16875501d51}

Cet exemple de code définit l’état de publication d’une ressource.

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
