---
description: Type de tâche pour autoriser l’exportation autorisée de fichiers précédemment téléchargés.
seo-description: Type de tâche pour autoriser l’exportation autorisée de fichiers précédemment téléchargés.
seo-title: ExportJob
solution: Experience Manager
title: ExportJob
topic: Scene7 Image Production System API
uuid: 439e3dd8-85b8-4f5b-abf8-8cc5a3f59fe6
translation-type: tm+mt
source-git-commit: 26fb6212c3106deb7b088020d9f2993e40dec20b

---


# ExportJob{#exportjob}

Type de tâche pour autoriser l’exportation autorisée de fichiers précédemment téléchargés.

ExportJob ne prend pas en charge les types de ressource suivants :

* Visionneuses d’images
* Visionneuses de rendus
* Visionneuses à 360°
* Visionneuses de supports
* Visionneuses à débit binaire multiple
* Visionneuses de vidéos
* Catalogues électroniques
* Visionneuses d’offres

<table id="table_D8F3FD30D15648BFA5B980D3DC0A5AB1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nom </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> assetHandleArray</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> type:HandleArray</span> </p> </td> 
   <td colname="col3" valign="top"> <p> de <span class="codeph"> fichierHandle</span> qui doivent être exportés. Voir <a href="../../types/c-data-types/r-handle-array.md#reference-1b93fefb5477459faf9253b54349b5f9" type="reference" format="dita" scope="local"> HandleArray</a>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fmt</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>Spécifie le type <span class="codeph"> export.Valeurs</span>possibles : [orig, convert] </p> <p> 
     <ul id="ul_16EF4B14100C4C7AA464CA9CF7F11D1C"> 
      <li id="li_DAB2844CC55145C88A18A1F8EC4527F9">Si <span class="codeph"> fmt=orig</span>, les actifs sont exportés en tant qu’éléments d’origine. </li> 
      <li id="li_07F2F8D159934D889FDC1022AB12B564">Si <span class="codeph"> fmt=convert</span>, les ressources sont converties au format spécifié dans les paramètres d’entrée <span class="codeph"> is_modifer</span> ou <span class="codeph"> macro</span> . </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> is_modifier</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>Indique la chaîne URL de rendu <span class="codeph"> ImageServer</span> , qui est ajoutée à la demande de conversion <span class="codeph"> ExportJob</span> Convertir. </p> <p>Pour plus d’informations sur l’envoi des modificateurs IS, reportez-vous à la documentation <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/" scope="external" format="html"></a> IS. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> macro</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p></p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> paramètre</span> de courrier électronique </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>Choix du paramètre de courrier électronique. Valeurs possibles : </p> <p> 
     <ul id="ul_0EEDAE11B7CD4C53A6E4B2B8CB2CF730"> 
      <li id="li_F235F93828594ED78C6D464440F953FF"> <span class="codeph"> Tout</span> </li> 
      <li id="li_59E14E7EBFA64432A5FAC15DA21A0521"> <span class="codeph"> Erreur</span> </li> 
      <li id="li_BFE0B52CADD14CC1BA1AF42AB0AA1CE1"> <span class="codeph"> ErrorAndWarning</span> </li> 
      <li id="li_BE3AA67E14FB487B8B9CD6EF3D58824C"> <span class="codeph"> Fin de tâche</span> </li> 
      <li id="li_409C68AD0D244975BFB86B08609E0146"> <span class="codeph"> Aucun</span> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> clientId</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>Indique l’adresse IP du client ou du client qui a initié la demande d’exportation. </p> <p> <p>Remarque :  ce paramètre n’est pas renseigné activement actuellement et est strictement réservé à une utilisation ultérieure uniquement. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

Dans le cas des demandes ExportJob, où `fmt=convert` et à la fois `is_modifier` et `macro` sont fournies, le fichier de destination respecte le format fourni par `macro`. Par exemple :

```
input_file = fileToExport.jpg
is_modifer = &fmt=png
macro=$test$ 
output_file = fileToExport.tiff
```

