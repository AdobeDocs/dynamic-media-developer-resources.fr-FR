---
description: Renvoie les contextes de publication pour les ressources marquées pour publication.
solution: Experience Manager
title: batchGetAssetPublishContexts
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: ba1f62a7-2698-4300-b6de-6d07ac764b0c
TQID: 'https://experienceleague.adobe.com/ei78NEtlPaqhT6Vf-jreBAxzfGcwGbxMLSsOfSb-Ym4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 96
ht-degree: 14%

---

# batchGetAssetPublishContexts{#batchgetassetpublishcontexts}

Renvoie les contextes de publication pour les ressources marquées pour publication.

Syntaxe

## Types d’utilisateurs autorisés {#section-d5362ca8a6ab42949cd648ba38dbf2f8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>* L’utilisateur doit disposer d’un accès en lecture pour renvoyer les ressources.
>* Tous les utilisateurs ont accès à la société partagée.
>

## Paramètres {#section-1742fcb196224545b270eb8241f757a8}

**Input (batchGetAssetPublishContextsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Gérer vers la société. |
| assetHandleArray | ` `types:HandleArray« | Oui | Liste des ressources que vous souhaitez interroger pour rechercher des contextes actifs (marqués pour publication). |

**Output (batchGetAssetPublishContextsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| assetPublishContextsArray | `types:assetPublishContextsArray` | Oui | Tableau de contextes de publication dans lesquels chaque ressource est marquée pour publication. |

## Exemples {#section-457f6809ccfa425b9a0976313d613f4e}

**Requête**

```java {.line-numbers}
<batchGetAssetPublishContextsParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <companyHandle>c|301</companyHandle>
  <assetHandleArray>
    <items>a|27007</items>
    <items>a|27008</items>
  </assetHandleArray>
</batchGetAssetPublishContextsParam>
```

**Réponse**

```java {.line-numbers}
<batchGetAssetPublishContextsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <assetPublishContextsArray>
    <items>
      <assetHandle>a|27007</assetHandle>
      <publishContextArray>
        <items>
          <contextHandle>pc|3002</contextHandle>
          <contextName>ImageServing</contextName>
          <contextType>ImageServing</contextType>
        </items>
      </publishContextArray>
    </items>
    <items>
      <assetHandle>a|27008</assetHandle>
      <publishContextArray>
        <items>
          <contextHandle>pc|3004</contextHandle>
          <contextName>Video</contextName>
          <contextType>Video</contextType>
        </items>
        <items>
          <contextHandle>pc|3001</contextHandle>
          <contextName>ImageRendering</contextName>
          <contextType>ImageRendering</contextType>
        </items>
      </publishContextArray>
    </items>
  </assetPublishContextsArray>
</batchGetAssetPublishContextsReturn>
```

