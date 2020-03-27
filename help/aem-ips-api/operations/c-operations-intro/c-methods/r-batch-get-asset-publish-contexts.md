---
description: Renvoie le  de publication pour les fichiers marqués pour publication.
seo-description: Renvoie le  de publication pour les fichiers marqués pour publication.
seo-title: batchGetAssetPublishContextes
solution: Experience Manager
title: batchGetAssetPublishContextes
topic: Scene7 Image Production System API
uuid: 7f442019-37a9-4473-be92-a952a7a67664
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# batchGetAssetPublishContextes{#batchgetassetpublishcontexts}

Renvoie le  de publication pour les fichiers marqués pour publication.

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
>* L’utilisateur doit disposer d’un accès en lecture pour renvoyer les fichiers.
>* Tous les utilisateurs ont accès au  partagé.
>



## Paramètres {#section-1742fcb196224545b270eb8241f757a8}

**Entrée (batchGetAssetPublishContextesParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui | Pose le . |
| ` *`assetHandleArray`*` | ` `types:HandleArray&quot; | Oui |  de ressources que vous souhaitez  pour le  actif (marqué pour publication). |

**Output (batchGetAssetPublishContextesReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`assetPublishContextesArray`*` | `types:assetPublishContextsArray` | Oui | Tableau de  de publication dans lequel chaque fichier est marqué pour publication. |

## Exemples {#section-457f6809ccfa425b9a0976313d613f4e}

**Request**

```java
<batchGetAssetPublishContextsParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <companyHandle>c|301</companyHandle>
  <assetHandleArray>
    <items>a|27007</items>
    <items>a|27008</items>
  </assetHandleArray>
</batchGetAssetPublishContextsParam>
```

**Réponse**

```java
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

