---
description: Obtient des jeux de propriétés associés à une poignée de type.
seo-description: Obtient des jeux de propriétés associés à une poignée de type.
seo-title: getPropertySet
solution: Experience Manager
title: getPropertySet
topic: Scene7 Image Production System API
uuid: fa3cadb3-92b3-4ffb-ac1e-87a01b98bcb2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getPropertySet{#getpropertysets}

Obtient des jeux de propriétés associés à une poignée de type.

Syntaxe

## Types d’utilisateurs autorisés {#section-da858360b72941bfa8d9558b4da7d4da}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-d8da2847e77e4a95a4441d9848cac775}

**Input (getPropertySetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`typeHandle`*` | `xsd:string` | Oui | poignée du type de jeu de propriétés. |
| ` *`mainPropriétairePrincipal`*` | `xsd:string` | Oui | Propriétaire principal des données liées à l’objet de base de données. |
| ` *`secondaryOwnerHandle`*` | `xsd:string` | Non | Propriétaire secondaire facultatif des données. |

**Output (getPropertySetReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`setArray`*` | `types:PropertySetArray` | Oui | Arborescence de jeux de propriétés. |

## Exemples {#section-1358af974eab4259864910337a6f0bd2}

Cet exemple de code renvoie des jeux de propriétés de leur propriétaire principal, spécifiés par une poignée de type.

**Request**

```java
<getPropertySetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
   <primaryOwnerHandle>u|41|strangio@adobe.com</primaryOwnerHandle>
</getPropertySetsParam>
```

**Réponse**

```java
<getPropertySetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setArray>
      <items>
         <setHandle>ps|941</setHandle>
         <typeHandle>pt|10801</typeHandle>
         <propertyArray>
            <items>
               <name>application_server_prefix_published_test</name>
               <value>http://s7teton.macromedia.com:8080/is/image/</value>
            </items>
            <items>
               <name>application_project_whatever</name>
               <value>false</value>
            </items>
            <items>
               <name>application_server_prefix_origin_test</name>
               <value>http://s7teton:8080/is/image</value>
            </items>
         </propertyArray>
      </items>
   </setArray>
</getPropertySetsReturn>
```

