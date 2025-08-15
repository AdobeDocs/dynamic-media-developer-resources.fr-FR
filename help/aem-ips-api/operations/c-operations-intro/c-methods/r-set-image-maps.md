---
description: Définit la zone cliquable d’un fichier.
solution: Experience Manager
title: ZoneCartes
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0c8e6536-0b9c-4fcc-b71f-511afc670089
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 10%

---

# ZoneCartes{#setimagemaps}

Définit la zone cliquable d’un fichier.

Vous devez déjà avoir créé les zones cliquables. Les zones cliquables sont appliquées dans l’ordre de récupération à partir de la matrice. Cela signifie que la deuxième zone cliquable recouvre la première, la troisième superpose la seconde, etc.

## Types d’utilisateurs autorisés {#section-adb21c5b679249939dd83816e4a0ee97}

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
| CompanyHandle | `xsd:string` | Oui | Pseudo de l’entreprise. |
| AssetHandle | `xsd:string` | Oui | Gestion des ressources. |
| Tableau d’images | `types:ImageMapDefinitionArray` | Oui | Tableau de zones cliquables prédéfinies. |

**Output (setImageMapsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| imageMapHandleArray | `types:HandleArray` | Oui | Tableau avec poignées de zone cliquable appliquées à la ressource. |

## Exemples {#section-fe2e35662a6a4ee29cf250c9fd180371}

Cet échantillon de code définit 2 zones cliquables pour un actif image. Le code spécifie le type de forme, la région et l’action effectuée lorsque les zones cliquables sont appelées. La réponse contient un tableau avec des descripteurs vers les zones cliquables.

**Demander**

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
