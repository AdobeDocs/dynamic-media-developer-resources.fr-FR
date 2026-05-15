---
description: Les jeux de propriétés sont des ensembles de paires nom-valeur spécifiques à l'application, qui peuvent être associés à divers objets IPS, selon le type de jeu de propriétés. Si le type de jeu de propriétés ne permet pas d’associer plusieurs jeux à un objet (PropertySetType/allowMultipleisfalse) et que l’objet est déjà associé à un jeu du même type, le nouveau jeu remplace le jeu existant.
solution: Experience Manager
title: createPropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e9f85e65-4a2f-4b82-b7b8-d0d60b8345cd
TQID: 'https://experienceleague.adobe.com/kMRKY0OQPDLsPpPDtTQpxwTBiBu3dco37mSxR7khfgg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 217
ht-degree: 7%

---

# createPropertySet{#createpropertyset}

Les jeux de propriétés sont des ensembles de paires nom-valeur spécifiques à l&#39;application, qui peuvent être associés à divers objets IPS, selon le type de jeu de propriétés. Si le type de jeu de propriétés ne permet pas d’associer plusieurs jeux à un objet (PropertySetType/allowMultipleisfalse) et que l’objet est déjà associé à un jeu du même type, le nouveau jeu remplace le jeu existant.

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
| typeHandle | `xsd:string` | Oui | Pointez sur le type de jeu de propriétés. |
| primaryOwnerHandle | `xsd:string` | Oui | Identificateur du propriétaire principal du jeu de propriétés. |
| secondaryOwnerHandle | `xsd:string` | Non | Poignée vers le propriétaire secondaire du jeu de propriétés. |
| propertyArray | `types:PropertyArray` | Oui | Le tableau des propriétés. |
| permissionArray | `types:PermissionUpdateArray` |  |  |

**Output (createPropertySetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| setHandle | `xsd:string` | Oui | La poignée du nouveau jeu de propriétés. |

## Exemples {#section-4e1f5b2883664bc88f590fcd253df22b}

Cet exemple de code crée un jeu de propriétés qui contient les noms et les valeurs des propriétés. La réponse renvoie une poignée au nouveau jeu de propriétés.

**Requête**

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
