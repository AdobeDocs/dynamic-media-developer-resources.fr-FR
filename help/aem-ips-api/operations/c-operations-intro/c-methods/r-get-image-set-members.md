---
description: Obtient un tableau des membres d’une visionneuse d’images.
solution: Experience Manager
title: getImageSetMembers
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 29ceef8b-127f-4460-8623-c3e26c959327
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 17%

---

# getImageSetMembers{#getimagesetmembers}

Obtient un tableau des membres d’une visionneuse d’images.

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

**Entrée (getImageSetMembersParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Gestionnaire de la société qui contient la visionneuse d’images. |
| assetHandle | `xsd:string` | Oui | Gestionnaire de ressources de la visionneuse d’images. |

**Sortie (getImageSetMembersReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| memberArray | `types:ImageSetMemberArray` | Non | Tableau des membres de la visionneuse d’images. |

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
