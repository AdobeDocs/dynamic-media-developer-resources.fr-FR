---
description: Cette section décrit la syntaxe de base du protocole HTTP de rendu d’image Dynamic Media.
solution: Experience Manager
title: Image Rending HTTP, protocole syntaxe de base
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 3%

---


# Rendu d’image syntaxe de base du protocole HTTP{#image-rendering-http-protocol-basic-syntax}

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
   <td colname="col2"> <p><span class="varname"> server_address</span> [:<span class="varname"> port</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> vignette  </span> </p> </td> 
   <td colname="col2"> <p>Spécificateur de vignette (chemin d’accès relatif au fichier ou entrée de catalogue de vignettes). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> modificateurs </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> modificateur</span> *[ &amp;  <span class="varname"> modificateur</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> modificateur </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> commande</span> | { $  <span class="varname"> macro</span> $ } | { .<span class="varname"> comment</span> } </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> command  </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="varname"> cmdName</span> | { $<span class="varname"> var</span> } } [ = <span class="varname"> valeur</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> macro  </span> </p> </td> 
   <td colname="col2"> <p>Nom d’une macro de commande. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> commentaire  </span> </p> </td> 
   <td colname="col2"> <p>Chaîne de commentaires (ignorée par le serveur). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> cmdName  </span> </p> </td> 
   <td colname="col2"> <p>Nom d’une commande ou d’un attribut. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> var </span> </p> </td> 
   <td colname="col2"> <p>Nom d’une variable personnalisée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> value  </span> </p> </td> 
   <td colname="col2"> <p>Valeur de commande ou de variable. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`server`*,  *`cmdName`*,  *`macro`* et  *`var`* ne tiennent pas compte de la casse. Le serveur conserve la casse de toutes les autres valeurs de chaîne.

**Identificateur du serveur**

Le contexte racine &quot; `/ir/render`&quot; est requis pour toutes les requêtes HTTP au rendu d’image.

**Commentaires**

Les commentaires peuvent être incorporés dans des chaînes de requête n’importe où et sont identifiés par un point (.) immédiatement après le séparateur de commandes (&amp;). Le commentaire se termine par l’occurrence suivante d’un séparateur de commande (non codé). Cette fonction peut être utilisée pour ajouter des informations à la demande qui ne sont pas destinées à la diffusion d’images, telles que des horodatages, des ID de base de données, etc.

**Décodage HTTP**

Le rendu d’image extrait d’abord *`object`* et *`modifiers`* de la requête entrante. *`object`* est ensuite séparé en éléments de chemin qui sont décodés individuellement par HTTP. La chaîne *`modifiers`* est séparée en paires *`command`*= *`value`* et *`value`* est alors décodée via HTTP avant le traitement spécifique à la commande.
