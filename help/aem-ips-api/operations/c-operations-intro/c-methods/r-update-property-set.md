---
description: Utilise un tableau de propriétés pour mettre à jour un jeu de propriétés.
solution: Experience Manager
title: updatePropertySet
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 14%

---


# updatePropertySet{#updatepropertyset}

Utilise un tableau de propriétés pour mettre à jour un jeu de propriétés.

Syntaxe

## Types d’utilisateur autorisés {#section-116693bbfb5d44219e62bbb1ba19de96}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-98361b063e9c41e8b2f744fabc0e13ed}

**Entrée (updatePropertySetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`setHandle`*` | `xsd:string` | Oui | Traitez le jeu de propriétés. |
| `*`replaceProperties`*` | `xsd:string` | Non | Définissez sur `true` pour remplacer les propriétés. |
| `*`propertyArray`*` | `types:PropertyArray` | Oui | Tableau des propriétés mises à jour pour le jeu de propriétés. |

**Output (updatePropertySetReturn)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-55d1c9dcd0174c6b9b52b4709f7c8bf9}

Cet exemple de code met à jour un jeu de propriétés avec des propriétés dans le tableau de propriétés.

**Request**

```java
<updatePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
   <replaceProperties>true</replaceProperties>
   <propertyArray>
      <items>
         <name>application_project_whatever</name>
         <value>false</value>
      </items>
      <items>
         <name>application_server_prefix_published_test</name>
         <value>http://s7teton.macromedia.com:8080/is/image/</value>
      </items>
      <items>
         <name>application_server_prefix_origin_test</name>
         <value>http://s7teton:8080/is/image/</value>
      </items>
   </propertyArray>
</updatePropertySetParam>
```

**Réponse**

Aucune
