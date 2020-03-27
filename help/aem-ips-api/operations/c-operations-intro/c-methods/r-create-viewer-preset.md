---
description: Crée un  prédéfini qui détermine ce qu’un utilisateur peut voir. Le lecteur peut être de tout type disponible dans IPS. Le  prédéfini est appliqué lorsque les fichiers sont publiés.
seo-description: Crée un  prédéfini qui détermine ce qu’un utilisateur peut voir. Le lecteur peut être de tout type disponible dans IPS. Le  prédéfini est appliqué lorsque les fichiers sont publiés.
seo-title: createViewerPreset
solution: Experience Manager
title: createViewerPreset
topic: Scene7 Image Production System API
uuid: 4160d2b0-6147-459f-830a-43c99b8dc196
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb

---


# createViewerPreset{#createviewerpreset}

Crée un  prédéfini qui détermine ce qu’un utilisateur peut voir. Le lecteur peut être de tout type disponible dans IPS. Le  prédéfini est appliqué lorsque les fichiers sont publiés.

Syntaxe

## Types d’utilisateurs autorisés {#section-0b8b1322ebea4a7ea24d516e080b7367}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-aa6dc37e327541ebbfed7685cd8071ff}

**Entrée (createViewerPresetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui | Poignée du  qui contient les paramètres prédéfinis et les ressources de la visionneuse. |
| ` *`folderHandle`*` | `xsd:string` | Oui | Identifiant du dossier contenant les ressources. |
| ` *`nom`*` | `xsd:string` | Oui | Nom de la visionneuse. |
| ` *`type`*` | `xsd:string` | Oui | Type de visionneuse. |
| ` *`configSettingArray`*` | `types:ConfigSettingArray` | Non | Tableau contenant les noms, les valeurs et les poignées des images auxquelles vous appliquez des paramètres prédéfinis. |

**Output (createViewerPresetReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`viewerPresetHandle`*` | `xsd:string` | Oui | Traitement du paramètre prédéfini dans la visionneuse. |

## Exemples {#section-c88ea63536f3461cbe4677ba53f875dd}

Cet exemple de code crée un paramètre prédéfini de lecteur vidéo. La réponse renvoie une poignée au paramètre prédéfini.

```java
<createViewerPresetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|0</companyHandle>
   <folderHandle>Scene7SharedAssets/</folderHandle>
   <name>eVideo4</name>
   <type>VideoPlayer</type>
   <configSettingArray>
      <items>
         <name>Video Bit Rate</name>
         <value>393334.6508779093</value>
      </items>
      <items>
         <name>Audio Sample Rate</name>
         <value>44100</value>
      </items>
      ...
      <items>
         <name>vidPaneWidth</name>
         <value>0</value>
      </items>
   </configSettingArray>
</createViewerPresetParam>
```

**Réponse**

```java
<createViewerPresetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <viewerPresetHandle>a|151760|40|151760</viewerPresetHandle>
</createViewerPresetReturn>
```

