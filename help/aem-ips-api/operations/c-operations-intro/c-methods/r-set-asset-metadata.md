---
description: Définit les valeurs de métadonnées d’un fichier. Fonctionne avec un tableau de mises à jour de métadonnées pour définir des valeurs dans un lot.
solution: Experience Manager
title: setAssetMetadata
feature: Dynamic Media Classic, SDK/API, Métadonnées, Gestion des ressources
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 9%

---


# setAssetMetadata{#setassetmetadata}

Définit les valeurs de métadonnées d’un fichier. Fonctionne avec un tableau de mises à jour de métadonnées pour définir des valeurs dans un lot.

Syntaxe

## Types d’utilisateur autorisés {#section-9dcacb0c924044648f8324bfed183dca}

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
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée vers la société avec la ressource à mettre à jour. |
| `*`assetHandle`*` | `xsd:string` | Oui | Poignée de la ressource. |
| `*`updateArray`*` | `types:MetadataUpdateArray` | Oui | Mises à jour dans un tableau de mise à jour des métadonnées. |

**Output (setAssetMetadataReturn)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

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
