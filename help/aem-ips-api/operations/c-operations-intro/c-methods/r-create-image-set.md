---
description: Crée une visionneuse d’images.
solution: Experience Manager
title: createImageSet
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 01ccc705-97e4-4e75-a322-e24bb78cb496
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 15%

---

# createImageSet{#createimageset}

Crée une visionneuse d’images.

Syntaxe

## Types d’utilisateurs autorisés {#section-58bf5027e6d24ab5a9fcba59776d15dc}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L’utilisateur doit disposer d’un accès en lecture/écriture au dossier de destination.

## Paramètres {#section-03d22ba7d290477e91c25ca1d4439200}

**Entrée (createImageSetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Gestionnaire de la société à laquelle appartient la visionneuse d’images. |
| folderHandle | `xsd:string` | Oui | Gestionnaire du dossier. |
| name | `xsd:string` | Oui | Nom de la visionneuse d’images. |
| type | `xsd:string` | Oui | Type de visionneuse d’images. |
| thumbAssetHandle | `xsd:string` | Non | Gestion de la ressource qui agit comme miniature de la nouvelle visionneuse d’images. S’il n’est pas spécifié, IPS tente d’utiliser la première ressource d’image référencée par la visionneuse. |

**Sortie**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| assetHandle | `xsd:string` | Oui | Gestion de la nouvelle visionneuse d’images. |

## Exemples {#section-385fe3b0af8044b0a2451336ec137fc5}

Cet exemple de code crée un jeu d’images spécifié par l’entreprise, le dossier, le nom et le type. La réponse est un gestionnaire de ressources de la visionneuse d’images nouvellement créée.

**Request**

```java
<ns1:createImageSetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/eCatalogs/</ns1:folderHandle>
   <ns1:name>My Image Set</ns1:name>
   <ns1:type>ImageSet</ns1:type>
</ns1:createImageSetParam>
```

**Réponse**

```java
<createImageSetReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <assetHandle>25741|22|841</assetHandle>
</createImageSetReturn>
```
