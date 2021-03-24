---
description: Définit la zone cliquable d’un fichier.
solution: Experience Manager
title: setImageMaps
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 10%

---


# setImageMaps{#setimagemaps}

Définit la zone cliquable d’un fichier.

Vous devez avoir déjà créé les zones cliquables. Les zones cliquables sont appliquées dans l&#39;ordre de récupération de la baie. Cela signifie que la deuxième zone cliquable recouvre la première, la troisième, la seconde, etc.

## Types d’utilisateur autorisés {#section-adb21c5b679249939dd83816e4a0ee97}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-2292ec1aead947ef8741dd0653a41f42}

**Entrée (setImageMapsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée de société. |
| `*`assetHandle`*` | `xsd:string` | Oui | Poignée de ressource. |
| `*`imageMapArray`*` | `types:ImageMapDefinitionArray` | Oui | Tableau de zones cliquables prédéfinies. |

**Output (setImageMapsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`imageMapHandleArray`*` | `types:HandleArray` | Oui | Tableau avec des poignées de zone cliquable appliquées à la ressource. |

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

