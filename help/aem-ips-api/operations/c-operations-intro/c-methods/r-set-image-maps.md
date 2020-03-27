---
description: Définit la zone cliquable d’un fichier.
seo-description: Définit la zone cliquable d’un fichier.
seo-title: setImageMaps
solution: Experience Manager
title: setImageMaps
topic: Scene7 Image Production System API
uuid: 1dd7e032-34b4-464d-8ec6-7ad282d12891
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setImageMaps{#setimagemaps}

Définit la zone cliquable d’un fichier.

Vous devez avoir déjà créé les zones cliquables. Les zones cliquables sont appliquées dans l’ordre de récupération à partir du tableau. Cela signifie que la deuxième zone cliquable se superpose à la première, la troisième à la seconde, etc.

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
| ` *`companyHandle`*` | `xsd:string` | Oui |  poignée. |
| ` *`assetHandle`*` | `xsd:string` | Oui | Poignée de ressource. |
| ` *`imageMapArray`*` | `types:ImageMapDefinitionArray` | Oui | Tableau de zones cliquables prédéfinies. |

**Output (setImageMapsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`imageMapHandleArray`*` | `types:HandleArray` | Oui | Tableau avec des poignées de zone cliquable appliquées au fichier. |

## Exemples {#section-fe2e35662a6a4ee29cf250c9fd180371}

Cet exemple de code définit 2 zones cliquables pour un fichier d’image. Le code spécifie le type de forme, la région et l’action effectuée lorsque les zones cliquables sont appelées. La réponse contient un tableau avec des poignées pour les zones cliquables.

**Request**

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

