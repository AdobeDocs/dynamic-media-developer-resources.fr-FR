---
title: Syntaxe de base du protocole HTTP de rendu d’image
description: Cette section décrit la syntaxe de base du protocole HTTP de rendu d’image Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8bf5920a-7ada-4db5-9796-05c5a17532c8
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 4%

---

# Syntaxe de base du protocole HTTP de rendu d’image{#image-rendering-http-protocol-basic-syntax}

Cette section décrit la syntaxe de base du protocole HTTP de rendu d’image Dynamic Media.

<table id="table_0A7D7207EE6D4B08B62BE8620EBE0B25"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Article </p> </th> 
   <th colname="col2" class="entry"> <p>Définition </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> request</span> </p> </td> 
   <td colname="col2"> <p>http://<span class="varname"> server</span>/ir/render[/<span class="varname"> vignette</span> ] [ ?<span class="varname"> modificateurs</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> server </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> server_address</span> [ :<span class="varname"> port</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> vignette </span> </p> </td> 
   <td colname="col2"> <p>Spécificateur de vignette (chemin de fichier relatif ou entrée de catalogue de vignettes). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> modificateurs </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> modifier</span> *[ &amp; <span class="varname"> modifier</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> modificateur </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> command</span> | { $ <span class="varname"> macro</span> $ } | { .<span class="varname"> comment</span> } </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> command </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="varname"> cmdName</span> | { $<span class="varname"> var</span> } [ = <span class="varname"> value</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> macro </span> </p> </td> 
   <td colname="col2"> <p>Nom d’une macro de commande. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> comment </span> </p> </td> 
   <td colname="col2"> <p>Chaîne de commentaire (ignorée par le serveur). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> cmdName </span> </p> </td> 
   <td colname="col2"> <p>Nom d’une commande ou d’un attribut. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> var </span> </p> </td> 
   <td colname="col2"> <p>Nom d’une variable personnalisée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> value </span> </p> </td> 
   <td colname="col2"> <p>Valeur de commande ou de variable. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`server`*, *`cmdName`*, *`macro`*, et *`var`* ne sont pas sensibles à la casse. Le serveur conserve la casse de toutes les autres valeurs string.

**Identifiant du serveur**

Le &quot; `/ir/render`Le contexte racine est requis pour toutes les requêtes HTTP vers le rendu d’image.

**Commentaires**

Les commentaires peuvent être incorporés dans des chaînes de requête n’importe où et sont identifiés par un point (.) juste après le séparateur de commande (&amp;). Le commentaire est terminé par l’occurrence suivante d’un séparateur de commande (non codé). Cette fonctionnalité peut être utilisée pour ajouter des informations à la requête qui ne sont pas destinées à un usage du serveur d’images, telles que les horodatages et les identifiants de base de données.

**Décodage HTTP**

Premiers extractions du rendu d’image *`object`* et *`modifiers`* de la requête entrante. Le *`object`* est ensuite séparé en éléments de chemin d’accès qui sont individuellement décodés par HTTP. Le *`modifiers`* chaîne est séparée en *`command`*= *`value`* paires et *`value`* est alors décodé via HTTP avant traitement spécifique à la commande.
