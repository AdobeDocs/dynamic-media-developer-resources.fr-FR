---
description: Les ensembles de propriétés sont des ensembles de paires nom-valeur spécifiques à l'application qui peuvent être attachés à divers objets IPS, selon le type de jeu de propriétés. Si le type de jeu de propriétés n'autorise pas l'association de plusieurs jeux à un objet (PropertySetType/allowMultipleisfalse) et que l'objet a déjà un jeu associé du même type, le nouveau jeu remplace celui existant.
solution: Experience Manager
title: createPropertySet
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 8%

---


# createPropertySet{#createpropertyset}

Les ensembles de propriétés sont des ensembles de paires nom-valeur spécifiques à l&#39;application qui peuvent être attachés à divers objets IPS, selon le type de jeu de propriétés. Si le type de jeu de propriétés n&#39;autorise pas l&#39;association de plusieurs jeux à un objet (PropertySetType/allowMultipleisfalse) et que l&#39;objet a déjà un jeu associé du même type, le nouveau jeu remplace celui existant.

Syntaxe

## Types d’utilisateur autorisés {#section-f9b6187ba636475787c997fc27bb192a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-25258e75f5f3419bad165c797eb6cd8e}

**Entrée (createPropertySetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`typeHandle`*` | `xsd:string` | Oui | poignée du type de jeu de propriétés. |
| `*`primaryOwnerHandle`*` | `xsd:string` | Oui | Poignée du propriétaire Principal du jeu de propriétés. |
| `*`secondaryOwnerHandle`*` | `xsd:string` | Non | Handle du propriétaire secondaire du jeu de propriétés. |
| `*`propertyArray`*` | `types:PropertyArray` | Oui | Tableau de propriétés. |
| `*`permissionArray`*` | `types:PermissionUpdateArray` |  |  |

**Output (createPropertySetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`setHandle`*` | `xsd:string` | Oui | Handle du nouveau jeu de propriétés. |

## Exemples {#section-4e1f5b2883664bc88f590fcd253df22b}

Cet exemple de code crée un jeu de propriétés qui contient les noms et les valeurs des propriétés. La réponse renvoie une poignée au nouveau jeu de propriétés.

**Request**

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

