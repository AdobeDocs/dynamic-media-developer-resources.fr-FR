---
description: La syntaxe de base du protocole HTTP est la suivante.
solution: Experience Manager
title: Syntaxe de base du protocole HTTP Image Serving
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 1%

---


# Syntaxe de base du protocole HTTP Image Serving{#image-serving-http-protocol-basic-syntax}

La syntaxe de base du protocole HTTP est la suivante :

<table id="simpletable_854C20D4C42247B99D9F123543C17E7C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> demander</span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="filepath">http://<span class="varname"> server</span>/is/image[/<span class="varname"> object</span>][ ?<span class="varname"> modificateurs</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> server </span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address</span>[:<span class="varname"> port</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> objet</span> </span> </p></td> 
  <td class="stentry"> <p>Spécificateur d’objet source (chemin d’image ou entrée de catalogue d’images). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modificateurs</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modificateur</span>*[&amp;<span class="varname"> modificateur</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modifier</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">commande|{$<span class="varname"> macro</span>$}|{.<span class="varname"> comment</span>}</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> command</span> </span> </p> </td> 
  <td class="stentry"> <p>{<span class="varname"> cmdName</span>|{$<span class="varname"> var</span>}[=<span class="varname"> valeur</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> macro</span> </span> </p> </td> 
  <td class="stentry"> <p>Nom d’une macro de commande.</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> commentaire</span> </span> </p></td> 
  <td class="stentry"> <p>Chaîne de commentaires (ignorée par le serveur).</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cmdName</span> </span> </p></td> 
  <td class="stentry"> <p>Un des noms de commande ou d'attribut pris en charge.</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> var</span> </span> </p> </td> 
  <td class="stentry"> <p>Nom d’une variable personnalisée.</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> value</span> </span> </p></td> 
  <td class="stentry"> <p>Valeur de commande ou de variable. </p></td> 
 </tr> 
</table>

*`server_address`*,  *`cmdName`*,  *`macro`* et  *`var`* ne tiennent pas compte de la casse. Le serveur conserve la casse de toutes les autres valeurs de chaîne.

*`value`* est spécifique à la commande et peut se composer d’une ou plusieurs valeurs séparées par des virgules. Consultez la description des commandes individuelles pour plus de détails.

## Identifiant du serveur {#section-926ae55ddba14b8d952147a5fd701e14}

Le contexte racine [!DNL /is/image] est requis pour toutes les requêtes HTTP à Image Serving.

## Décodage HTTP {#section-20922baccd804d2d986b44ce9a183a7d}

Image Serving extrait d’abord *`object`* et *`modifiers`* de la requête entrante. *`object`* est ensuite séparé en éléments de chemin qui sont décodés individuellement par HTTP. La chaîne *`modifiers`* est séparée en paires *`command`*= *`value`* et *`value`* est alors décodée via HTTP avant le traitement spécifique à la commande.

>[!NOTE]
>
>Sauf indication contraire dans la documentation, tous les caractères dangereux doivent être codés selon la norme HTTP. Pour plus d’informations, voir la spécification HTTP.

## Commentaires {#section-69ef0be0f17a418c87a0eba21c2ddb00}

Les commentaires peuvent être incorporés dans des chaînes de requête n’importe où et sont identifiés par un point(.) immédiatement après le séparateur de commandes(&amp;). Le commentaire se termine par l’occurrence suivante d’un séparateur de commande (non codé). Cette fonctionnalité peut être utilisée pour ajouter des informations à la requête qui ne sont pas destinées à la diffusion d’images, telles que des horodatages et des ID de base de données.

## Voir aussi {#section-d0b836568c31454b8dbeb136e6bbe0f0}

[Types](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/c-data-types.md#concept-49455c12df954bb5919cdd8d5ccc85fa) de données, Spécifications  [HTTP/1.1](http://www.w3.org/Protocols/rfc2616/rfc2616.html)
