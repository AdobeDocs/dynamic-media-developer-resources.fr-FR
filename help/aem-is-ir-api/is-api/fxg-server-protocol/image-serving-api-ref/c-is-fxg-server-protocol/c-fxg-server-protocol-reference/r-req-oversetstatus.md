---
title: req
description: Type de requête. Spécifie le type de demande.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9242c873-5a85-4ede-82b6-4ef15feecf50
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---

# req{#req}

Type de requête. Spécifie le type de demande.

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
   <td colname="col2"> <p> Renvoie les erreurs lors du rendu de l’indicateur avec les modificateurs d’URL fournis. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des contenus </span> </p> </td> 
   <td colname="col2"> <p> Renvoyer la liste xml de tous les éléments avec une valeur d’attribut s7:element<span class="codeph"> </span> et une liste de toutes les pages du document fxg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> overetstatus </span> </p> </td> 
   <td colname="col2"> <p>Renvoie une liste XML dont <span class="codeph"> éléments &lt;RichText/&gt;</span> sont en excès. </p> <p>Renvoie une liste xml d’éléments <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> en excès pour le traitement côté client. Seuls <span class="+ topic/ph pr-d/codeph codeph"> éléments &lt;RichText/&gt;</span> en excès sont renvoyés. Le <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> est un attribut <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> obligatoire lors de l’utilisation de <span class="+ topic/ph pr-d/codeph codeph"> req=oversetstatus</span>. Les éléments <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> en excès sans <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> ne sont pas répertoriés. Chaque élément <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> de la liste comporte les <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>, <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> et le cadre de sélection du cadre de texte en excès. L’attribut <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> indique l’index de texte de l’article jusqu’auquel le texte a pu s’adapter dans le bloc. Le <span class="+ topic/ph pr-d/codeph codeph"> Req=oversetstatus</span> s’applique uniquement aux éléments <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> dans le fichier FXG demandé. Il ne répertorie aucun élément <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> provenant d’un FXG incorporé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> existe</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>Identifiant de requête unique reqId </p> <p>Elle renvoie une seule propriété nommée catalogRecord.exists. La valeur de la propriété est définie sur « 1 » si l’entrée de catalogue spécifiée existe dans l’image ou le catalogue par défaut, sinon elle est définie sur « 0 ». les requêtes req=exists par rapport au contexte /is/content indiquent la présence ou l'absence d'un enregistrement spécifié dans le catalogue de contenu statique. </p> </td> 
  </tr> 
 </tbody> 
</table>
