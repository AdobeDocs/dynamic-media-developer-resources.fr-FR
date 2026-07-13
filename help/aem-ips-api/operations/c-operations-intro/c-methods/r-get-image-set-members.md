---
description: Obtient un tableau des membres qui se trouvent dans une visionneuse d’images.
solution: Experience Manager
title: getImageSetMembers
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 29ceef8b-127f-4460-8623-c3e26c959327
TQID: 'https://experienceleague.adobe.com/7tS3wEIqaBPmykuVmDBfq9GugDcbnevj-XAQQHM3icY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 94
ht-degree: 14%

---

# getImageSetMembers{#getimagesetmembers}

Obtient un tableau des membres qui se trouvent dans une visionneuse d’images.

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
>Nécessite un accès en lecture à l’image et à la ressource de jeu de membres.

## Paramètres {#section-a67ba98095574533980997c83ceaa316}

**Input (getImageSetMembersParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | La poignée de la société qui contient la visionneuse d’images. |
| assetHandle | `xsd:string` | Oui | Gestionnaire de ressources de visionneuse d’images. |

**Output (getImageSetMembersReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| memberArray | `types:ImageSetMemberArray` | Non | Tableau des membres de la visionneuse d’images. |

## Exemples {#section-888a9a78033346f39b171229de93dfa0}

Cet exemple de code renvoie des membres de visionneuse d’images spécifiques. La réponse renvoie un tableau vide.

**Requête**

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

