---
description: Définit les commandes du protocole Image Serving ou Image Rendering pour la ressource spécifiée. Ces commandes modifient la représentation de la ressource sans la détruire.
solution: Experience Manager
title: setUrlModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9e96ffc8-5a38-46b8-9ba8-956c86b32c7a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 6%

---

# setUrlModifier{#seturlmodifier}

Définit les commandes du protocole Image Serving ou Image Rendering pour la ressource spécifiée. Ces commandes modifient la représentation de la ressource sans la détruire.

Pour le service d’images, les commandes du paramètre `urlModifier` sont publiées dans le champ Catalogue des modificateurs et appliquées avant toute commande spécifiée dans l’URL de la requête. Les commandes de `urlPostApplyModifier` sont publiées dans le champ de catalogue `PostModifier` et remplacent toutes les commandes de l’URL de demande ou dans `urlModifier`. Pour le rendu d’image, les commandes de `urlModifier` et `urlPostApplyModifier` sont concaténées et publiées dans le champ du catalogue des modificateurs .

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
| companyHandle | `xsd:string` | Oui | Poignée de la société. |
| assetHandle | `xsd:string` | Oui | Poignée de ressource. |
| urlModifier | `xsd:string` | Non | Commandes de protocole de diffusion d’images ou de rendu d’images à appliquer avant les commandes de requête ou de `urlPostApplyModifier`. |
| urlPostApplyModifier | `xsd:string` | Non | Commandes du protocole de diffusion d’images ou de rendu d’images à appliquer après les commandes `urlModifier` et de requête. |

**Sortie (setUrlModifierReturn)**

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
