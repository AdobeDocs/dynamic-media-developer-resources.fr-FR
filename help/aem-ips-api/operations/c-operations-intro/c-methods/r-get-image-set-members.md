---
description: Récupère un tableau de membres qui se trouvent dans une visionneuse d’images.
solution: Experience Manager
title: getImageSetMembers
feature: Dynamic Media Classic, SDK/API, visionneuses d’images
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 15%

---


# getImageSetMembers{#getimagesetmembers}

Récupère un tableau de membres qui se trouvent dans une visionneuse d’images.

Syntaxe

## Types d’utilisateur autorisés {#section-eaa3a167fa77403ea1b374b05fff4ded}

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
>Nécessite l’accès en lecture à l’image et au fichier de jeu de membres.

## Paramètres {#section-a67ba98095574533980997c83ceaa316}

**Entrée (getImageSetMembersParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée de la société contenant la visionneuse d’images. |
| `*`assetHandle`*` | `xsd:string` | Oui | Poignée de fichier de visionneuse d’images. |

**Output (getImageSetMembersReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`MemberArray`*` | `types:ImageSetMemberArray` | Non | Tableau des membres de la visionneuse d’images. |

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

