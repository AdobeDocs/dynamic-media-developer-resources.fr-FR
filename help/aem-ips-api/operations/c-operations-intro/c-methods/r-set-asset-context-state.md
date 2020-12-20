---
description: Définissez ou mettez à jour l’état de publication pour un ou plusieurs fichiers. Vous pouvez définir des états de publication distincts pour chaque contexte de publication dans une société.
seo-description: Définissez ou mettez à jour l’état de publication pour un ou plusieurs fichiers. Vous pouvez définir des états de publication distincts pour chaque contexte de publication dans une société.
seo-title: setAssetsContextState
solution: Experience Manager
title: setAssetsContextState
topic: Scene7 Image Production System API
uuid: 4b94f9ea-3f7b-45ee-9381-6434f2bc4e31
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 9%

---


# setAssetsContextState{#setassetscontextstate}

Définissez ou mettez à jour l’état de publication pour un ou plusieurs fichiers. Vous pouvez définir des états de publication distincts pour chaque contexte de publication dans une société.

## Types d’utilisateur autorisés {#section-815eb031f85143278c1560c18c5e3431}

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
>L’utilisateur doit disposer d’un accès en lecture pour renvoyer la ressource.

## Paramètres {#section-009b9006de8e4c16ad657c47f28ace9f}

**Entrée (setAssetsContextStateParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui | Pose la société. |
| ` *`assetsContextHandle`*` | `types:AssetsContextStateUpdateArray` | Oui | Tableau de ressources et de leurs nouveaux états de publication. |

**Sortie (setAssetsContextStateReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Oui | Le nombre de ressources a bien changé. |
| ` *`warningCount`*` | `xsd:int` | Oui | Nombre d’avertissements générés lorsque l’opération tentait de modifier des ressources. |
| ` *`errorCount`*` | `xsd:int` | Oui | Nombre d’erreurs générées lorsque l’opération tentait de modifier des ressources. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | Non | Tableau des erreurs générées par les ressources lorsque l’opération tentait de les modifier. |

## Exemples {#section-283a073f3cb14bcda5abed863c538aa4}

Cet exemple de code définit l&#39;état de publication d&#39;un fichier à l&#39;aide de `NotMarkedForPublish`.

**Request**

```java
<setAssetsContextStateParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <companyHandle>c|301</companyHandle>
  <assetsContextStateUpdateArray>
    <items>
      <assetHandle>a|27007</assetHandle>
      <contextStateUpdateArray>
        <items>
          <contextHandle>pc|3001</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3002</contextHandle>
          <publishState>MarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3003</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3004</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
      </contextStateUpdateArray>
    </items>
    <items>
      <assetHandle>a|27008</assetHandle>
      <contextStateUpdateArray>
        <items>
          <contextHandle>pc|3001</contextHandle>
          <publishState>MarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3002</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3003</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3004</contextHandle>
          <publishState>MarkedForPublish</publishState>
        </items>
      </contextStateUpdateArray>
    </items>
  </assetsContextStateUpdateArray>
</setAssetsContextStateParam>
```

**Réponse**

```java
<setAssetsContextStateReturn xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04-beta">
  <successCount>8</successCount>
  <warningCount>0</warningCount>
  <errorCount>0</errorCount>
</setAssetsContextStateReturn>
```

