---
description: Définit les commandes du protocole de diffusion d’images ou de rendu d’image pour la ressource spécifiée. Ces commandes modifient la représentation de la ressource sans la détruire.
seo-description: Définit les commandes du protocole de diffusion d’images ou de rendu d’image pour la ressource spécifiée. Ces commandes modifient la représentation de la ressource sans la détruire.
seo-title: setUrlModificateur
solution: Experience Manager
title: setUrlModificateur
topic: Scene7 Image Production System API
uuid: ec423e57-338b-4a32-be5a-a73fa96712ce
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setUrlModificateur{#seturlmodifier}

Définit les commandes du protocole de diffusion d’images ou de rendu d’image pour la ressource spécifiée. Ces commandes modifient la représentation de la ressource sans la détruire.

Pour la diffusion d’images, les commandes du `urlModifier` paramètre sont publiées dans le champ du catalogue des modificateurs et appliquées avant toute commande spécifiée dans l’URL de requête. Les commandes dans `urlPostApplyModifier` seront publiées dans le champ de `PostModifier` catalogue et remplaceront toutes les commandes de l’URL de demande ou `urlModifier`dans. Pour le rendu d’image, les commandes dans `urlModifier` et `urlPostApplyModifier` sont concaténées et publiées dans le champ du catalogue des modificateurs.

## Types d’utilisateurs autorisés {#section-fefcd732ccf64c78956606538f96c73d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-3304fe49bbe24ea1a886e19aaf41fb7d}

**Input (setUrlModificateurParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui |  poignée. |
| ` *`assetHandle`*` | `xsd:string` | Oui | Poignée de ressource. |
| ` *`urlModificateur`*` | `xsd:string` | Non | Commandes du protocole de diffusion d’images ou de rendu d’image à appliquer avant la demande ou les `urlPostApplyModifier` commandes. |
| ` *`urlPostApplyModificateur`*` | `xsd:string` | Non | Commandes du protocole de diffusion d’images ou de rendu d’image à appliquer après `urlModifier` et demander. |

**Output (setUrlModificateurReturn)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

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
