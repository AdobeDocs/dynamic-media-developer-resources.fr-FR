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
ht-degree: 7%

---

# setUrlModifier{#seturlmodifier}

Définit les commandes du protocole Image Serving ou Image Rendering pour la ressource spécifiée. Ces commandes modifient la représentation de la ressource sans la détruire.

Pour la diffusion d’images, les commandes de la fonction `urlModifier` sont publiés dans le champ Catalogue de modificateurs et appliqués avant toute commande spécifiée dans l’URL de la requête. Commandes dans `urlPostApplyModifier` sont publiées dans la variable `PostModifier` champ de catalogue et remplacez toutes les commandes de l’URL de requête ou dans `urlModifier`. Pour le rendu d’image, les commandes de la section `urlModifier` et `urlPostApplyModifier` sont concaténés et publiés dans le champ Catalogue de modificateurs .

## Types d’utilisateurs autorisés {#section-fefcd732ccf64c78956606538f96c73d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-3304fe49bbe24ea1a886e19aaf41fb7d}

**Entrée (setUrlModifierParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Poignée de la société. |
| assetHandle | `xsd:string` | Oui | Poignée de ressource. |
| urlModifier | `xsd:string` | Non | Commandes du protocole de diffusion d’images ou de rendu d’images à appliquer avant une demande ou `urlPostApplyModifier` des commandes. |
| urlPostApplyModifier | `xsd:string` | Non | Commandes du protocole Image Serving ou Image Rendering à appliquer après `urlModifier` et les commandes de requête. |

**Sortie (setUrlModifierReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-801d4b9b986443f59a5783a3d6bf44aa}

**Request**

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
