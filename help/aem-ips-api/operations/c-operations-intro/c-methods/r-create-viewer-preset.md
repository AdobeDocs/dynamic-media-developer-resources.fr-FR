---
description: Crée une vue prédéfinie qui détermine ce qu’un utilisateur peut voir. La visionneuse peut être de n’importe quel type disponible dans IPS. La vue prédéfinie est appliquée lorsque les ressources sont publiées.
solution: Experience Manager
title: createViewerPreset
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: b24536d9-df66-4c94-8467-6f46e66a1b36
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 12%

---

# createViewerPreset{#createviewerpreset}

Crée une vue prédéfinie qui détermine ce qu’un utilisateur peut voir. La visionneuse peut être de n’importe quel type disponible dans IPS. La vue prédéfinie est appliquée lorsque les ressources sont publiées.

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
| companyHandle | `xsd:string` | Oui | Gestionnaire de l’entreprise qui contient les paramètres prédéfinis de visionneuse et les ressources. |
| folderHandle | `xsd:string` | Oui | Gestionnaire du dossier contenant les ressources. |
| nom | `xsd:string` | Oui | Nom de la visionneuse. |
| type | `xsd:string` | Oui | Type de visionneuse. |
| configSettingArray | `types:ConfigSettingArray` | Non | Tableau contenant les noms, valeurs et poignées des images auxquelles vous appliquez des paramètres prédéfinis. |

**Sortie (createViewerPresetReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| viewerPresetHandle | `xsd:string` | Oui | Gérer le paramètre prédéfini à la visionneuse. |

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
