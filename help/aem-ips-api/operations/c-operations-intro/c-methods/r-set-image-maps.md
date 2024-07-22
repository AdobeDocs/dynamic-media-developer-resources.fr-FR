---
description: Définit la zone cliquable d’une ressource.
solution: Experience Manager
title: setImageMaps
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0c8e6536-0b9c-4fcc-b71f-511afc670089
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 10%

---

# setImageMaps{#setimagemaps}

Définit la zone cliquable d’une ressource.

Vous devez avoir déjà créé les zones cliquables. Les zones cliquables sont appliquées dans l’ordre de récupération à partir du tableau . Cela signifie que la seconde zone cliquable s’incruste la première, la troisième, la seconde, etc.

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
| companyHandle | `xsd:string` | Oui | Poignée de la société. |
| assetHandle | `xsd:string` | Oui | Poignée de ressource. |
| imageMapArray | `types:ImageMapDefinitionArray` | Oui | Tableau de zones cliquables prédéfinies. |

**Sortie (setImageMapsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| imageMapHandleArray | `types:HandleArray` | Oui | Un tableau avec des zones cliquables est appliqué à la ressource. |

## Exemples {#section-fe2e35662a6a4ee29cf250c9fd180371}

Cet exemple de code définit 2 zones cliquables pour une ressource image. Le code spécifie le type de forme, la région et l’action entreprise lors de l’appel des zones cliquables. La réponse contient un tableau contenant des poignées vers les zones cliquables.

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
