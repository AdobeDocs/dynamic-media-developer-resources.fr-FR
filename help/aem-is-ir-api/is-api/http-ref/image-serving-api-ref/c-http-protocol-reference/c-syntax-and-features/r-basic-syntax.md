---
description: La syntaxe de base du protocole HTTP est la suivante.
solution: Experience Manager
title: Syntaxe de base du protocole HTTP du service d’images
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac75d6d0-a71e-45a0-89ee-b952a0202793
source-git-commit: 92a995b6cbadb00a075a3be5ae2a9f8feb6c900d
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 1%

---

# Syntaxe de base du protocole HTTP du service d’images{#image-serving-http-protocol-basic-syntax}

La syntaxe de base du protocole HTTP est la suivante :

<table id="simpletable_854C20D4C42247B99D9F123543C17E7C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> demande </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="filepath">http://<span class="varname"> server</span>/is/image[/<span class="varname"> object</span>][ ?<span class="varname"> modificateurs</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> serveur <span class="varname"> </span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address</span>[:<span class="varname"> port</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> objet </span> </span> </p></td> 
  <td class="stentry"> <p>Spécificateur d’objet Source (chemin d’accès de l’image ou entrée du catalogue d’images). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modificateurs </span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modificateur</span>*[&amp;<span class="varname"> modificateur</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modifier </span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">commande|{$<span class="varname"> macro</span>$}|{.<span class="varname"> commentaire </span>}</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> commande </span> </span> </p> </td> 
  <td class="stentry"> <p><code>{</code><span class="varname"> valeur cmdName</span>|<code>{$</code><span class="varname"> var</span><code>}}[=</code><span class="varname"></span><code>]</code> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> macro</span> </span> </p> </td> 
  <td class="stentry"> <p>Nom d'une macro de commande.</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> commentaire </span> </span> </p></td> 
  <td class="stentry"> <p>Chaîne de commentaire (ignorée par le serveur).</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cmdName</span> </span> </p></td> 
  <td class="stentry"> <p>Un des noms de commande ou d’attribut pris en charge.</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> var</span> </span> </p> </td> 
  <td class="stentry"> <p>Nom d’une variable personnalisée.</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> valeur <span class="varname"> </span> </span> </p></td> 
  <td class="stentry"> <p>Valeur de commande ou de variable. </p></td> 
 </tr> 
</table>

*`server_address`*, *`cmdName`*, *`macro`* et *`var`* ne respectent pas la casse. Le serveur conserve la casse de toutes les autres valeurs de chaîne.

*`value`* est spécifique à une commande et peut se composer d’une ou de plusieurs valeurs séparées par des virgules. Reportez-vous à la description des commandes individuelles pour plus d’informations.

## Identifiant du serveur {#section-926ae55ddba14b8d952147a5fd701e14}

Le contexte racine [!DNL /is/image] est requis pour toutes les requêtes HTTP au service d’images.

## Décodage HTTP {#section-20922baccd804d2d986b44ce9a183a7d}

La diffusion d’images extrait d’abord *`object`* et *`modifiers`* de la requête entrante. *`object`* est ensuite séparé en éléments de chemin qui sont individuellement décodés en HTTP. La chaîne *`modifiers`* est séparée en paires *`command`*= *`value`*, puis *`value`* est décodée en HTTP avant le traitement spécifique à la commande.

>[!NOTE]
>
>Sauf indication contraire dans la documentation, tous les caractères dangereux doivent être codés selon la norme HTTP. Pour plus d’informations, consultez la spécification HTTP .

## Commentaires {#section-69ef0be0f17a418c87a0eba21c2ddb00}

Les commentaires peuvent être incorporés n’importe où dans les chaînes de requête et sont identifiés par un point (.) juste après le séparateur de commande (&amp;). Le commentaire se termine par l’occurrence suivante d’un séparateur de commande (non codé). Cette fonctionnalité peut être utilisée pour ajouter des informations à la requête qui ne sont pas destinées à la diffusion d’images, telles que des horodatages et des identifiants de base de données.

## Voir aussi {#section-d0b836568c31454b8dbeb136e6bbe0f0}

[Types de données](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/c-data-types.md#concept-49455c12df954bb5919cdd8d5ccc85fa), [Spécification HTTP/1.1](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
