---
description: Utilise un tableau de propriétés pour mettre à jour un jeu de propriétés.
solution: Experience Manager
title: Mettre à jour PropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: bbe6a664-b6e1-4b46-867d-a134070b13da
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 12%

---

# Mettre à jour PropertySet{#updatepropertyset}

Utilise un tableau de propriétés pour mettre à jour un jeu de propriétés.

Syntaxe

## Types d’utilisateurs autorisés {#section-116693bbfb5d44219e62bbb1ba19de96}

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
| Poignée setHandle | `xsd:string` | Oui | Poignée pour le jeu de propriétés. |
| Propriétés replaceProperties | `xsd:string` | Non | Définissez sur `true` pour remplacer les propriétés. |
| Tableau de propriété | `types:PropertyArray` | Oui | Tableau des propriétés mises à jour pour le jeu de propriétés. |

**Output (updatePropertySetReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-55d1c9dcd0174c6b9b52b4709f7c8bf9}

Cet exemple de code met à jour un ensemble de propriétés avec des propriétés dans le tableau de propriétés.

**Demander**

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
