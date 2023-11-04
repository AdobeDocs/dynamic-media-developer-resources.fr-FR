---
description: Les ensembles de propriétés sont des ensembles de paires nom-valeur spécifiques à l’application qui peuvent être joints à divers objets IPS, selon le type de jeu de propriétés. Si le type de jeu de propriétés ne permet pas que plusieurs jeux soient joints à un objet (PropertySetType/allowMultipleisfalse) et que l’objet a déjà un jeu associé du même type, le nouveau jeu remplace celui existant.
solution: Experience Manager
title: createPropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e9f85e65-4a2f-4b82-b7b8-d0d60b8345cd
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 8%

---

# createPropertySet{#createpropertyset}

Les ensembles de propriétés sont des ensembles de paires nom-valeur spécifiques à l’application qui peuvent être joints à divers objets IPS, selon le type de jeu de propriétés. Si le type de jeu de propriétés ne permet pas que plusieurs jeux soient joints à un objet (PropertySetType/allowMultipleisfalse) et que l’objet a déjà un jeu associé du même type, le nouveau jeu remplace celui existant.

Syntaxe

## Types d’utilisateurs autorisés {#section-f9b6187ba636475787c997fc27bb192a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-25258e75f5f3419bad165c797eb6cd8e}

**Entrée (createPropertySetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| typeHandle | `xsd:string` | Oui | La gestion du type de jeu de propriétés. |
| primaryOwnerHandle | `xsd:string` | Oui | Gestionnaire du propriétaire principal de l’ensemble de propriétés. |
| secondaryOwnerHandle | `xsd:string` | Non | Gestionnaire du propriétaire secondaire du jeu de propriétés. |
| propertyArray | `types:PropertyArray` | Oui | Tableau de propriétés. |
| permissionArray | `types:PermissionUpdateArray` |  |  |

**Sortie (createPropertySetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| setHandle | `xsd:string` | Oui | La gestion du nouveau jeu de propriétés. |

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
