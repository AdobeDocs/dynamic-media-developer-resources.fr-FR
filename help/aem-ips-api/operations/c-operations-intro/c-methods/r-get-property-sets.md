---
description: Obtient des jeux de propriétés associés à un type handle.
solution: Experience Manager
title: getPropertySets
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: da6923c3-9b86-4595-8205-645fb10e03b0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 18%

---

# getPropertySets{#getpropertysets}

Obtient des jeux de propriétés associés à un type handle.

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

**Entrée (getPropertySetsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| typeHandle | `xsd:string` | Oui | La gestion du type de jeu de propriétés. |
| primaryOwnerHandle | `xsd:string` | Oui | Propriétaire Principal des données liées à l’objet de base de données. |
| secondaryOwnerHandle | `xsd:string` | Non | Propriétaire secondaire facultatif des données. |

**Sortie (getPropertySetsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| setArray | `types:PropertySetArray` | Oui | Fichier de jeux de propriétés. |

## Exemples {#section-1358af974eab4259864910337a6f0bd2}

Cet exemple de code renvoie les ensembles de propriétés de leur propriétaire Principal, spécifiés par un type handle.

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
