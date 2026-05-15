---
title: Syntaxe de base du protocole HTTP de rendu d'image
description: Cette section décrit la syntaxe de base du protocole HTTP de rendu d’image Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8bf5920a-7ada-4db5-9796-05c5a17532c8
TQID: 'https://experienceleague.adobe.com/v-ucFAnnoq6ywaB97QSXodqnO4VWFvaK6I2HJ2-a4Fc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 227
ht-degree: 0%

---

# Syntaxe de base du protocole HTTP de rendu d&#39;image{#image-rendering-http-protocol-basic-syntax}

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
   <td colname="col1"> <p><span class="varname"> demande </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> server</span>/ir/render[/<span class="varname"> vignette</span> ] [ ?<span class="varname"> modificateurs </span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p></span> du serveur <span class="varname"> </p> </td> 
   <td colname="col2"> <p><span class="varname"> server_address </span> [ :<span class="varname"> port</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> vignette </span> </p> </td> 
   <td colname="col2"> <p>Spécificateur de vignette (chemin de fichier relatif ou entrée de catalogue de vignette). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> des modifications </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> modificateur </span> *[ et <span class="varname"> modificateur </span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p></span> du modificateur <span class="varname"> </p> </td> 
   <td colname="col2"> <p><span class="varname"> commande </span> | { $ <span class="varname"> macro</span> $ } | { .<span class="varname"> comment </span> } </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p></span> de commande <span class="varname"> </p> </td> 
   <td colname="col2"> <p>{ <span class="varname"> cmdName</span> | { $<span class="varname"> var</span> } } [ = <span class="varname"> valeur </span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p></span> de macro <span class="varname"> </p> </td> 
   <td colname="col2"> <p>Nom d'une macro de commande. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> commentaire </span> </p> </td> 
   <td colname="col2"> <p>Chaîne de commentaire (ignorée par le serveur). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p></span> <span class="varname"> cmdName </p> </td> 
   <td colname="col2"> <p>Nom d’une commande ou d’un attribut. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> var </span> </p> </td> 
   <td colname="col2"> <p>Nom d’une variable personnalisée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p></span> de la valeur <span class="varname"> </p> </td> 
   <td colname="col2"> <p>Valeur de commande ou de variable. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`server`*, *`cmdName`*, *`macro`* et *`var`* ne respectent pas la casse. Le serveur conserve la casse de toutes les autres valeurs de chaîne.

**Identifiant du serveur**

Le contexte racine « `/ir/render` » est requis pour toutes les requêtes HTTP vers le rendu d’image.

**Commentaires**

Les commentaires peuvent être incorporés dans des chaînes de requête n’importe où et sont identifiés par un point (.) juste après le séparateur de commandes (&amp;). Le commentaire se termine par l’occurrence suivante d’un séparateur de commande (non codé). Cette fonction peut être utilisée pour ajouter des informations à la requête qui ne sont pas destinées à la diffusion d’images, telles que des horodatages et des identifiants de base de données.

**Décodage HTTP**

Le rendu d’image extrait d’abord le *`object`* et le *`modifiers`* de la requête entrante. Le *`object`* est ensuite séparé en éléments de chemin qui sont individuellement décodés en HTTP. La chaîne *`modifiers`* est séparée en paires *`command`*= *`value`*, puis *`value`* est décodée en HTTP avant le traitement spécifique à la commande.
