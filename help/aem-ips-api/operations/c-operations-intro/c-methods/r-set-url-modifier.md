---
description: Définit les commandes du protocole de diffusion d’images ou de rendu d’image pour la ressource spécifiée. Ces commandes modifient la représentation de la ressource sans la détruire.
solution: Experience Manager
title: setUrlModificateur
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 7%

---


# setUrlModificateur{#seturlmodifier}

Définit les commandes du protocole de diffusion d’images ou de rendu d’image pour la ressource spécifiée. Ces commandes modifient la représentation de la ressource sans la détruire.

Pour la diffusion d’images, les commandes du paramètre `urlModifier` sont publiées dans le champ du catalogue de modificateurs et appliquées avant toute commande spécifiée dans l’URL de requête. Les commandes de `urlPostApplyModifier` seront publiées dans le champ de catalogue `PostModifier` et remplaceront toutes les commandes de l&#39;URL de demande ou de `urlModifier`. Pour le rendu d’image, les commandes de `urlModifier` et `urlPostApplyModifier` sont concaténées et publiées dans le champ du catalogue de modificateurs.

## Types d’utilisateur autorisés {#section-fefcd732ccf64c78956606538f96c73d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-3304fe49bbe24ea1a886e19aaf41fb7d}

**Entrée (setUrlModificateurParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée de société. |
| `*`assetHandle`*` | `xsd:string` | Oui | Poignée de ressource. |
| `*`urlModificateur`*` | `xsd:string` | Non | Commandes du protocole Image Serving ou Image Rendering à appliquer avant la commande request ou `urlPostApplyModifier`. |
| `*`urlPostApplyModificateur`*` | `xsd:string` | Non | Commandes du protocole Image Serving ou Image Rendering à appliquer après `urlModifier` et les commandes request. |

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
