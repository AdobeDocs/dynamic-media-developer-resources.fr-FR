---
description: Un proxy de serveur d’images peut être utilisé pour redimensionner les images des téléphones japonais.
solution: Experience Manager
title: proxy de serveur d’images
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0389a4af-a412-42eb-b7b4-716e47d623a0
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---

# proxy de serveur d’images{#image-server-proxy}

Un proxy de serveur d’images peut être utilisé pour redimensionner les images des téléphones japonais.

## Format URL {#section-2e8c40b0547c4f99874cdf502b338940}

Le format d’URL du proxy IS est très similaire aux requêtes IS standard. Tout modificateur IS transmis au proxy est transmis au serveur d’images. Vous trouverez des informations sur les modificateurs IS dans la variable [Référence du protocole HTTP](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-introduction/c-introduction.md#concept-dbbd5241bc6248ad9b9d7f6c635c311e).

`http://<server>/is-proxy/image/<company><asset>?<modifiers>`

`http://<server>/is-proxy/image/sample/chair?qlt=75`

## Liste de modificateurs spécifique au proxy {#section-1bff28f9cf5b4e04a31308b06176ee5f}

<table id="simpletable_40C1DFB183B54A79BCF65D51ED480CE0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> Largeur = &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Indique le pourcentage de la largeur utilisable de l’appareil comme largeur d’image. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> heipercent = &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Indique le pourcentage de la hauteur utilisable de l’appareil comme hauteur d’image. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> sizepercent = &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Indique le pourcentage de la propriété Memory Limit Embedded Media de l’appareil à limiter la taille de la réponse à . Cela s’applique uniquement aux réponses jpg. La qualité de l’image est réduite jusqu’à ce que la taille de la réponse soit comprise dans le pourcentage spécifié. </p></td> 
 </tr> 
</table>

## Limite de mémoire d’image incorporée {#section-52f7c69ed8a341ceabf92ceee19b0f36}

Si l’appareil est limité à la taille des images pouvant être incorporées sur une page web, la taille de l’image est limitée à cette taille tant que le format de réponse est jpg. Le proxy limite les réponses à 500 Mo si l’appareil n’a pas de limite.

## Traitement en arrière-plan {#section-bdf7c294b6824de9969c97fc1f8aa6d3}

Le proxy télécharge, vérifie et charge le fichier de données Device Atlas une fois par jour. La vérification extrait différentes propriétés pour différents appareils et les compare aux valeurs attendues avant d’accepter les nouvelles données.
