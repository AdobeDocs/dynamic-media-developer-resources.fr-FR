---
description: Supprime le champ de métadonnées d’une entreprise.
solution: Experience Manager
title: deleteMetadataField
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1922fc1b-2abc-4d31-985a-65c788af4d46
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 11%

---

# deleteMetadataField{#deletemetadatafield}

Supprime le champ de métadonnées d’une entreprise.

Syntaxe

## Types d’utilisateurs autorisés {#section-63e7d17f4b434995a872838bfff7f9ff}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-73f12a30cc4340b6b32dd11effd5195e}

**Entrée (deleteMetadataFieldParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Gestionnaire de la société qui contient le champ de métadonnées à supprimer. |
| fieldHandle | `xsd:string` | Oui | La gestion du champ de métadonnées à supprimer. |

**Sortie (deleteMetadataFieldParam)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-e1c474ea91a040609ecd7c2400f4fa3c}

Cet exemple de code supprime le champ de métadonnées d’une entreprise. Elle utilise le nom d’entreprise et le nom de métadonnées comme champs dans la variable `deleteMetadataFieldParam` transmis au serveur des services Web IPS pour effectuer cette action.

**Request**

```java
<deleteMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
</deleteMetadataFieldParam>
```

**Réponse**

Aucun.0
