---
description: Utilise un tableau de propriétés pour mettre à jour un jeu de propriétés.
solution: Experience Manager
title: updatePropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: bbe6a664-b6e1-4b46-867d-a134070b13da
TQID: 'https://experienceleague.adobe.com/-z-ZUe9SO-HG05Gv6XQAlREi2wrP93lH-HFEwNOxENI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 85
ht-degree: 12%

---

# updatePropertySet{#updatepropertyset}

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

**Input (updatePropertySetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| setHandle | `xsd:string` | Oui | Gérer vers le jeu de propriétés. |
| replaceProperties | `xsd:string` | Non | Définissez sur `true` pour remplacer les propriétés. |
| propertyArray | `types:PropertyArray` | Oui | Tableau des propriétés mises à jour pour le jeu de propriétés. |

**Output (updatePropertySetReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-55d1c9dcd0174c6b9b52b4709f7c8bf9}

Cet exemple de code met à jour une propriété définie avec des propriétés dans le tableau de propriétés.

**Requête**

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
