---
description: Crée une visionneuse d’images.
solution: Experience Manager
title: createImageSet
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 14%

---


# createImageSet{#createimageset}

Crée une visionneuse d’images.

Syntaxe

## Types d’utilisateur autorisés {#section-58bf5027e6d24ab5a9fcba59776d15dc}

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
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée de la société à laquelle appartient la visionneuse d’images. |
| `*`folderHandle`*` | `xsd:string` | Oui | Identifiant du dossier. |
| `*`name`*` | `xsd:string` | Oui | Nom de la visionneuse d’images. |
| `*`type`*` | `xsd:string` | Oui | Type de visionneuse d’images. |
| `*`thumbAssetHandle`*` | `xsd:string` | Non | Gestion du fichier qui agit comme miniature pour la nouvelle visionneuse d’images. S’il n’est pas spécifié, IPS tente d’utiliser le premier fichier d’image référencé par la visionneuse. |

**Sortie**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Oui | Poignée de la nouvelle visionneuse d’images. |

## Exemples {#section-385fe3b0af8044b0a2451336ec137fc5}

Cet exemple de code crée une visionneuse d’images spécifiée par société, dossier, nom et type. La réponse est un gestionnaire de ressources de la visionneuse d’images nouvellement créée.

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

