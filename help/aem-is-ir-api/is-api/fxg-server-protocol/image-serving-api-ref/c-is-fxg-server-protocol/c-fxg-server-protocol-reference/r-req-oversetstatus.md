---
title: req
description: Type de requête. Indique le type de requête.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9242c873-5a85-4ede-82b6-4ef15feecf50
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 2%

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
   <td colname="col2"> <p> Renvoie la liste xml de tous les éléments avec une <span class="codeph"> s7:element</span> et une liste de toutes les pages du document fxg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> overversetstatus</span> </p> </td> 
   <td colname="col2"> <p>Renvoie une liste XML de laquelle <span class="codeph"> &lt;richtext /&gt;</span> Les éléments sont exagérés. </p> <p>Renvoie une liste xml de <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> éléments surconfigurés pour le traitement côté client. Uniquement <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> les éléments surconfigurés sont renvoyés. La variable <span class="+ topic/ph pr-d/codeph codeph"> s7:elementd</span> est obligatoire <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> lors de l’utilisation de <span class="+ topic/ph pr-d/codeph codeph"> req=oversetstatus</span>. Tout excès <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> éléments sans <span class="+ topic/ph pr-d/codeph codeph"> s7:elementd</span> n’est pas répertoriée. Chaque <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> La propriété <span class="+ topic/ph pr-d/codeph codeph"> s7:elementd</span>, <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span>et le cadre de sélection du cadre de texte en excès. La variable <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> indique l’index de texte dans l’article à la hauteur du texte pouvant tenir dans le cadre. La variable <span class="+ topic/ph pr-d/codeph codeph"> Req=oversetstatus</span> s’applique uniquement à <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> dans le FXG demandé. Elle ne répertorie pas les <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> des éléments de tout FXG incorporé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> existe</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>Identifiant de requête unique reqId </p> <p>Elle renvoie une propriété unique nommée catalogRecord.exists. La valeur de la propriété est définie sur "1" si l’entrée de catalogue spécifiée existe dans l’image ou le catalogue par défaut, sinon elle est définie sur "0". Les requêtes req=exists par rapport au contexte /is/content indiquent la présence ou l’absence d’un enregistrement spécifié dans le catalogue de contenu statique. </p> </td> 
  </tr> 
 </tbody> 
</table>
