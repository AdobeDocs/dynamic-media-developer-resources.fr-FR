---
description: Définit les valeurs de métadonnées d’une ressource. Fonctionne avec un tableau de mises à jour de métadonnées pour définir des valeurs dans un lot.
solution: Experience Manager
title: setAssetMetadata
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 811e44e1-774a-49bd-a2bd-a7504e5f7f5f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 10%

---

# setAssetMetadata{#setassetmetadata}

Définit les valeurs de métadonnées d’une ressource. Fonctionne avec un tableau de mises à jour de métadonnées pour définir des valeurs dans un lot.

Syntaxe

## Types d’utilisateurs autorisés {#section-9dcacb0c924044648f8324bfed183dca}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L’utilisateur doit disposer d’un accès en lecture à la ressource.

## Paramètres {#section-bcdcff30905e444388811e897b2824bd}

**Entrée (setAssetMetadataParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Gestionnaire de l’entreprise avec la ressource que vous souhaitez mettre à jour. |
| assetHandle | `xsd:string` | Oui | Gestionnaire de la ressource. |
| updateArray | `types:MetadataUpdateArray` | Oui | Mises à jour dans un tableau de mise à jour de métadonnées. |

**Sortie (setAssetMetadataReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-1ab412e7ee1d4d6d8469b0b403598c42}

Cet exemple de code utilise un tableau de mises à jour de métadonnées pour définir les métadonnées de la ressource spécifiée.

**Request**

```java
<ns1:setAssetMetadataParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
   <ns1:updateArray>
      <ns1:items>
         <ns1:fieldHandle>47|ALL|Resolution</ns1:fieldHandle>
         <ns1:value>320</ns1:value>
      </ns1:items>
   </ns1:updateArray>
</ns1:setAssetMetadataParam>
```

**Réponse**

Aucune
