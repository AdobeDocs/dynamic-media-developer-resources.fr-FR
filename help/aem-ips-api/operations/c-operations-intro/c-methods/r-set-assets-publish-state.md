---
description: Détermine si un lot de ressources est prêt à être publié.
solution: Experience Manager
title: setAssetsPublishState
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: dce324e4-cf86-4a65-ab00-8cd2bba20f8f
TQID: 'https://experienceleague.adobe.com/VV11khRodimEOAdPB-6mHR-gIT4AMiKOKeuuH6J15VA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 151
ht-degree: 11%

---

# setAssetsPublishState{#setassetspublishstate}

Détermine si un lot de ressources est prêt à être publié.

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
>L’utilisateur doit disposer d’un accès en lecture et écriture à la ressource.

## Paramètres {#section-3e49d7859f8647b990d75373cc8dbc24}

**Input (setAssetsPublishStateParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Identifiant de la société. |
| publishStateUpdateArray | `types:PublishStateUpdateArray` | Oui | Tableau de valeurs d’état de publication des ressources. |

**Output (setAssetsPublishStateParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| successCount | `xsd:int` | Oui | Nombre de ressources mises à jour. |
| warningCount | `xsd:int` | Oui | Nombre de ressources qui ont généré un avertissement lorsque l’opération a tenté de les mettre à jour. |
| errorCount | `xsd:int` | Oui | Nombre de ressources ayant généré une erreur lorsque l’opération a tenté de les supprimer. |
| warningDetailArray | `types:AssetOperationFaultArray` | Non | Détails associés aux mises à jour des ressources ayant généré un avertissement. |
| errorDetailArray | `types:AssetOperationFaultArray` | Non | Détails associés aux mises à jour des ressources ayant généré une erreur. |

## Exemples {#section-38cfdd3436214a06a1bae16875501d51}

Cet exemple de code définit le statut de publication d’une ressource.

**Requête**

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
