---
description: Obtient un tableau de membres qui se trouvent dans une visionneuse d’images.
seo-description: Obtient un tableau de membres qui se trouvent dans une visionneuse d’images.
seo-title: getImageSetMembers
solution: Experience Manager
title: getImageSetMembers
topic: Scene7 Image Production System API
uuid: b19c9fec-df92-42e1-9228-42cdf196fdfc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getImageSetMembers{#getimagesetmembers}

Obtient un tableau de membres qui se trouvent dans une visionneuse d’images.

Syntaxe

## Types d’utilisateurs autorisés {#section-eaa3a167fa77403ea1b374b05fff4ded}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Nécessite un accès en lecture à l’image et à la ressource du jeu de membres.

## Paramètres {#section-a67ba98095574533980997c83ceaa316}

**Input (getImageSetMembersParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui | Poignée du  qui contient la visionneuse d’images. |
| ` *`assetHandle`*` | `xsd:string` | Oui | Poignée de fichier de la visionneuse d’images. |

**Output (getImageSetMembersReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`MemberArray`*` | `types:ImageSetMemberArray` | Non | Tableau des membres de la visionneuse d’images. |

## Exemples {#section-888a9a78033346f39b171229de93dfa0}

Cet exemple de code renvoie des membres de visionneuse d’images spécifiques. La réponse renvoie un tableau vide.

**Request**

```java
<ns1:getImageSetMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>34195|22|927</ns1:assetHandle>
</ns1:getImageSetMembersParam>
```

**Réponse**

```java
<getImageSetMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <memberArray></memberArray>
</getImageSetMembersReturn>
```

