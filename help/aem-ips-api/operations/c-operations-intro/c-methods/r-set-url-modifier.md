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

Pour Image Server, les commandes du `urlModifier` paramètre sont publiées dans le champ Modificateur catalog et appliquées avant toute commande spécifiée dans l’URL de requête. Les commandes de `urlPostApplyModifier` sont publiées dans le champ de `PostModifier` catalogue et remplacent toutes les commandes de l’URL de requête ou dans `urlModifier`. Pour Image Rendering, les commandes dans `urlModifier` et `urlPostApplyModifier` sont concaténées et publiées dans le champ Modificateur catalogue.

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
| CompanyHandle | `xsd:string` | Oui | Pseudo de l’entreprise. |
| AssetHandle | `xsd:string` | Oui | Gestion des ressources. |
| Modificateur d’url | `xsd:string` | Non | Commandes du protocole Image Serving ou Image Rendering à appliquer avant la ou `urlPostApplyModifier` les commandes. |
| urlPostApplyModifier | `xsd:string` | Non | Commandes du protocole Image Serving ou Image Rendering à appliquer après `urlModifier` et à requérir. |

**Output (setUrlModifierReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-801d4b9b986443f59a5783a3d6bf44aa}

**Demander**

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
