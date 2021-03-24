---
description: Regroupez les fichiers dans des jeux à l’aide d’un tableau de liste de descripteurs de ressources.
solution: Experience Manager
title: AutomatedSetGenerationJob
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 7%

---


# AutomatedSetGenerationJob{#automatedsetgenerationjob}

Regroupez les fichiers dans des jeux à l’aide d’un tableau de liste de descripteurs de ressources.

Syntaxe

## Paramètres {#section-939b2e6946a64238be3709fec2cd0b84}

<table id="table_0E031B2014B646BDA2A94D7E0B55DD5B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nom </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:HandleArray</span> </td> 
   <td colname="col3">Tableau de gestionnaires de ressources utilisés pour créer la visionneuse. <p>Par défaut, 1 000 correspond au nombre maximal de ressources que vous pouvez avoir dans la baie. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> destFolder</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Chemin d’accès au dossier dans lequel vous souhaitez enregistrer les visionneuses. Enregistre dans le dossier racine de société par défaut. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Définit un indicateur pour indiquer si les fichiers doivent être publiés ou non. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:AutoSetCreationOptions</span> </td> 
   <td colname="col3">Tableau de scripts de génération de visionneuses que vous pouvez exécuter sur les fichiers téléchargés. Voir <a href="../../types/c-data-types/r-auto-set-creation-options.md#reference-58b42b39e53345aeb87cd1adc864e7ff" format="dita" scope="local"> AutoSetCreationOptions</a></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Configurez une notification électronique automatisée pour la tâche. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Options emailSetting**

Le paramètre `emailSetting` comprend les options suivantes :

| Option | Retours |
|---|---|
| `All` | Toutes les notifications de tâche (erreurs, avertissements, achèvement) au destinataire spécifié. |
| `Error` | Erreurs de tâche au destinataire spécifié. |
| `ErrorAndWarning` | Erreurs de tâche et avertissements au destinataire spécifié. |
| `JobCompletion` | Notification de fin de tâche au destinataire spécifié. |
| `None` | La tâche n&#39;envoie aucune notification de tâche à l&#39;destinataire spécifié. |

## Exemple {#section-d01ee7671f274a1fa12737e8df91d2cf}

```
<complexType name="AutomatedSetGenerationJob">
  <sequence>
    <element name="assetHandleArray" type="types:HandleArray"/>
    <element name="destFolder" type="xsd:string" minOccurs="0"/>
    <element name="readyForPublish" type="xsd:boolean"/>
    <element name="autoSetCreationOptions" type="types:AutoSetCreationOptions"/>
    <element name="emailSetting" type="xsd:string"/>
  </sequence>
</complexType>
```

