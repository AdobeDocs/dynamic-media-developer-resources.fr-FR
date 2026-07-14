---
description: Définit la zone cliquable d’une ressource.
solution: Experience Manager
title: setImageMaps
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0c8e6536-0b9c-4fcc-b71f-511afc670089
TQID: 'https://experienceleague.adobe.com/sOGDO0ruTEK1DS5Sc-4nhLfViddEKCLDLJlpC-8H3g0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 134
ht-degree: 10%

---

# setImageMaps{#setimagemaps}

Définit la zone cliquable d’une ressource.

Vous devez avoir déjà créé les zones cliquables. Les zones cliquables sont appliquées dans l’ordre de récupération à partir du tableau . Cela signifie que la deuxième zone cliquable recouvre la première, que la troisième recouvre la deuxième, etc.

## Types d’utilisateurs autorisés {#section-adb21c5b679249939dd83816e4a0ee97}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-2292ec1aead947ef8741dd0653a41f42}

**Input (setImageMapsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Identifiant de la société. |
| assetHandle | `xsd:string` | Oui | Identifiant de ressource. |
| imageMapArray | `types:ImageMapDefinitionArray` | Oui | Tableau de zones cliquables prédéfinies. |

**Output (setImageMapsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| imageMapHandleArray | `types:HandleArray` | Oui | Tableau avec des descripteurs de zone cliquable appliqués à la ressource. |

## Exemples {#section-fe2e35662a6a4ee29cf250c9fd180371}

Cet exemple de code définit 2 zones cliquables pour une ressource image. Le code spécifie le type de forme, la région et l&#39;action effectuée lorsque les zones cliquables sont appelées. La réponse contient un tableau avec des descripteurs pour les zones cliquables.

**Requête**

```java
<setImageMapsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|739|1|537</assetHandle>
   <imageMapArray>
      <items>
         <name>ImageMap2</name>
         <shapeType>Rectangle</shapeType>
         <region>40</region>
         <action>400</action>
         <enabled>true</enabled>
      </items>
      <items>
         <name>ImageMap3</name>
         <shapeType>Rectangle</shapeType>
         <region>40</region>
         <action>400</action>
         <enabled>false</enabled>
      </items>
   </imageMapArray>
</setImageMapsParam>
```

