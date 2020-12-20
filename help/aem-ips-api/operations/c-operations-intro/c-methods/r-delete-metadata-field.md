---
description: Supprime un champ de métadonnées de société.
seo-description: Supprime un champ de métadonnées de société.
seo-title: deleteMetadataField
solution: Experience Manager
title: deleteMetadataField
topic: Scene7 Image Production System API
uuid: 06ec434a-2793-4227-ac93-ae3871c38ab9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 10%

---


# deleteMetadataField{#deletemetadatafield}

Supprime un champ de métadonnées de société.

Syntaxe

## Types d’utilisateur autorisés {#section-63e7d17f4b434995a872838bfff7f9ff}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-73f12a30cc4340b6b32dd11effd5195e}

**Entrée (deleteMetadataFieldParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui | Poignée de la société contenant le champ de métadonnées à supprimer. |
| ` *`fieldHandle`*` | `xsd:string` | Oui | Poignée du champ de métadonnées à supprimer. |

**Output (deleteMetadataFieldParam)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-e1c474ea91a040609ecd7c2400f4fa3c}

Cet exemple de code supprime un champ de métadonnées de société. Il utilise le nom d&#39;utilisateur de la société et le nom de métadonnées comme champs dans le `deleteMetadataFieldParam` transmis au serveur de services Web IPS pour effectuer cette action.

**Request**

```java
<deleteMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
</deleteMetadataFieldParam>
```

**Réponse**

Aucun.0
