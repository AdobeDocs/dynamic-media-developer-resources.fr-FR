---
description: Renvoie les contextes de publication des ressources marquées pour publication.
solution: Experience Manager
title: batchGetAssetPublishContexts
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: ba1f62a7-2698-4300-b6de-6d07ac764b0c
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 16%

---

# batchGetAssetPublishContexts{#batchgetassetpublishcontexts}

Renvoie les contextes de publication des ressources marquées pour publication.

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

**Entrée (batchGetAssetPublishContextsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Gérer la société. |
| assetHandleArray | ` `types:HandleArray&quot; | Oui | Liste des ressources que vous souhaitez interroger pour des contextes principaux (marqués pour publication). |

**Sortie (batchGetAssetPublishContextsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| assetPublishContextsArray | `types:assetPublishContextsArray` | Oui | Tableau de contextes de publication dans lequel chaque ressource est marquée pour publication. |

## Exemples {#section-457f6809ccfa425b9a0976313d613f4e}

**Request**

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
