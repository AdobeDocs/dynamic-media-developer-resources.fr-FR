---
description: Définit les commandes de protocole de diffusion d’images ou de rendu d’images pour la ressource spécifiée. Ces commandes modifient la représentation de la ressource sans la détruire.
solution: Experience Manager
title: setUrlModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9e96ffc8-5a38-46b8-9ba8-956c86b32c7a
TQID: 'https://experienceleague.adobe.com/dcz-gnw7NjHKN7EvsGvSRDmu4dgCUo2PPr3GjYLVoOA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 175
ht-degree: 6%

---

# setUrlModifier{#seturlmodifier}

Définit les commandes de protocole de diffusion d’images ou de rendu d’images pour la ressource spécifiée. Ces commandes modifient la représentation de la ressource sans la détruire.

Pour la diffusion d’images, les commandes du paramètre `urlModifier` sont publiées dans le champ Catalogue des modificateurs et appliquées avant toute commande spécifiée sur l’URL de la requête. Dans `urlPostApplyModifier`, les commandes sont publiées dans le champ Catalogue de `PostModifier` et remplacent toutes les commandes sur l’URL de la requête ou dans `urlModifier`. Pour le rendu d’image, les commandes dans `urlModifier` et `urlPostApplyModifier` sont concaténées et publiées dans le champ Catalogue des modificateurs .

## Types d’utilisateurs autorisés {#section-fefcd732ccf64c78956606538f96c73d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-3304fe49bbe24ea1a886e19aaf41fb7d}

**Input (setUrlModifierParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Identifiant de la société. |
| assetHandle | `xsd:string` | Oui | Identifiant de ressource. |
| urlModifier | `xsd:string` | Non | Commandes de protocole de diffusion d’images ou de rendu d’images à appliquer avant les commandes request ou `urlPostApplyModifier`. |
| urlPostApplyModifier | `xsd:string` | Non | Commandes de protocole de diffusion d’images ou de rendu d’images à appliquer après les commandes `urlModifier` et request. |

**Output (setUrlModifierReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-801d4b9b986443f59a5783a3d6bf44aa}

**Requête**

```java
<setUrlModifierParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|942|1|579</assetHandle>
   <urlModifier>modify=that</urlModifier>
   <urlPostApplyModifier>action=awesomeToo</urlPostApplyModifier>
</setUrlModifierParam>
```

**Réponse**

Aucune

