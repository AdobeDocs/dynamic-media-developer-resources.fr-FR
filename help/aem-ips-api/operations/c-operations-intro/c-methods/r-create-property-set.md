---
description: Les ensembles de propriétés sont des ensembles de paires nom-valeur spécifiques à l’application qui peuvent être attachés à divers objets IPS, en fonction du type de jeu de propriétés. Si le type de jeu de propriétés n’autorise pas l’attachement de plusieurs ensembles à un objet (PropertySetType/allowMultipleisfalse) et que l’objet est déjà associé à un jeu du même type, le nouvel ensemble remplace le jeu existant.
solution: Experience Manager
title: Créer un ensemble de propriétés
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e9f85e65-4a2f-4b82-b7b8-d0d60b8345cd
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 7%

---

# Créer un ensemble de propriétés{#createpropertyset}

Les ensembles de propriétés sont des ensembles de paires nom-valeur spécifiques à l’application qui peuvent être attachés à divers objets IPS, en fonction du type de jeu de propriétés. Si le type de jeu de propriétés n’autorise pas l’attachement de plusieurs ensembles à un objet (PropertySetType/allowMultipleisfalse) et que l’objet est déjà associé à un jeu du même type, le nouvel ensemble remplace le jeu existant.

Syntaxe

## Types d’utilisateurs autorisés {#section-f9b6187ba636475787c997fc27bb192a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-25258e75f5f3419bad165c797eb6cd8e}

**Input (createPropertySetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| Poignée de type | `xsd:string` | Oui | Poignée pour le type de jeu de propriétés. |
| PrimaryOwnerHandle | `xsd:string` | Oui | Poignée adressée au propriétaire principal du jeu de propriétés. |
| SecondaryOwnerHandle | `xsd:string` | Non | Poignée adressée au propriétaire secondaire du jeu de propriétés. |
| Tableau de propriété | `types:PropertyArray` | Oui | Tableau de propriétés. |
| Tableau d’autorisations | `types:PermissionUpdateArray` |  |  |

**Output (createPropertySetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| Poignée setHandle | `xsd:string` | Oui | Poignée du nouveau jeu de propriétés. |

## Exemples {#section-4e1f5b2883664bc88f590fcd253df22b}

Cet exemple de code crée un ensemble de propriétés qui contient les noms et les valeurs des propriétés. La réponse renvoie une poignée au nouveau jeu de propriétés.

**Demander**

```java
<createPropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
   <primaryOwnerHandle>u|41|strangio@adobe.com</primaryOwnerHandle>
   <propertyArray>
      <items>
         <name>application_project_whatever</name>
         <value>true</value>
      </items>
      <items>
         <name>application_server_prefix_published_test</name>
         <value>http://s7everest.macromedia.com:8080/is/image/</value>
      </items>
      <items>
         <name>application_server_prefix_origin_test</name>
         <value>http://s7everest:8080/is/image/</value>
      </items>
   </propertyArray>
</createPropertySetParam>
```

**Réponse**

```java
<createPropertySetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</createPropertySetReturn>
```
