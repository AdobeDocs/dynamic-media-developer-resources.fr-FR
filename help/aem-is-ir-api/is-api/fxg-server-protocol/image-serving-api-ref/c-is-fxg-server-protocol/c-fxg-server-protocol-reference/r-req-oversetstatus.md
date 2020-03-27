---
description: Type de requête. Indique le type de requête.
seo-description: Type de requête. Indique le type de requête.
seo-title: req
solution: Experience Manager
title: req
topic: Scene7 Image Serving - Image Rendering API
uuid: 1c8ff9c3-9f39-46a8-bd38-8e0c5ab0f548
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# req{#req}

Type de requête. Indique le type de requête.

`req={validate|contents|oversetstatus|exists}`

<table id="table_F39239E5244746DB9F253BB0D5E85D54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Valeur </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> valider</span> </p> </td> 
   <td colname="col2"> <p> Renvoie les erreurs de rendu du fichier fxg avec les modificateurs d’URL fournis. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> contenu</span> </p> </td> 
   <td colname="col2"> <p> Renvoie un xml de tous les éléments avec une valeur d’attribut <span class="codeph"> s7:element</span> et un de toutes les pages dans la  fxg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> overetstatus</span> </p> </td> 
   <td colname="col2"> <p>Renvoie un XML dont les éléments <span class="codeph"> &lt;RichText/&gt;</span> sont en excès. </p> <p>Renvoie un xml d’éléments <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> en excès pour traitement côté client. Seuls <span class="+ topic/ph pr-d/codeph codeph"> les éléments &lt;RichText/&gt;</span> en excès sont renvoyés. <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> est un attribut obligatoire <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> lorsque vous utilisez <span class="+ topic/ph pr-d/codeph codeph"> req=overetstatus</span>. Les éléments en excès <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> sans <span class="+ topic/ph pr-d/codeph codeph"> élémentScene7:elementd</span> ne sont pas répertoriés. Chaque <span class="+ topic/ph pr-d/codeph codeph"> élément</span> &lt;RichText/&gt; <span class="+ topic/ph pr-d/codeph codeph"> dans le  de comporte les éléments</span>s7:elementid <span class="+ topic/ph pr-d/codeph codeph"> ,</span>s7:endCharIndexet le cadre de sélection du bloc de texte en excès. L’attribut <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> indique l’index de texte dans l’article jusqu’auquel le texte a pu tenir dans le bloc. <span class="+ topic/ph pr-d/codeph codeph"> Req=overetstatus</span> s’applique uniquement aux éléments <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> dans le fichier FXG demandé. Il ne  aucun élément <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> issu d’un fichier FXG incorporé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> existe</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]]</span> </p> <p>Identifiant de requête unique reqId </p> <p>Renvoie une propriété unique nommée catalogRecord.exists. La valeur de la propriété est définie sur "1" si l’entrée de catalogue spécifiée existe dans l’image ou le catalogue par défaut, sinon elle est définie sur "0". les requêtes req=exists dans le contexte /is/content indiquent la présence ou l’absence d’un enregistrement spécifié dans le catalogue de contenu statique. </p> </td> 
  </tr> 
 </tbody> 
</table>

