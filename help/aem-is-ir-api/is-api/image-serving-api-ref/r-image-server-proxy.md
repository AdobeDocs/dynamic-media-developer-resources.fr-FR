---
description: Un proxy de serveur d’images peut être utilisé pour redimensionner les images pour les téléphones japonais.
seo-description: Un proxy de serveur d’images peut être utilisé pour redimensionner les images pour les téléphones japonais.
seo-title: Proxy de serveur d’images
solution: Experience Manager
title: Proxy de serveur d’images
topic: Scene7 Image Serving - Image Rendering API
uuid: 49aa0861-9b03-4a62-8604-67e6cb7a621f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---


# Proxy de serveur d’images{#image-server-proxy}

Un proxy de serveur d’images peut être utilisé pour redimensionner les images pour les téléphones japonais.

## Format URL {#section-2e8c40b0547c4f99874cdf502b338940}

Le format d’url pour le proxy IS est très similaire aux demandes IS régulières. Tout modificateur IS transmis au proxy est transmis au serveur d’images. Vous trouverez des informations sur les modificateurs IS dans la [Référence du protocole HTTP](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-introduction/c-introduction.md#concept-dbbd5241bc6248ad9b9d7f6c635c311e).

`http://<server>/is-proxy/image/<company><asset>?<modifiers>`

`http://<server>/is-proxy/image/sample/chair?qlt=75`

## Liste de modificateur spécifique au proxy {#section-1bff28f9cf5b4e04a31308b06176ee5f}

<table id="simpletable_40C1DFB183B54A79BCF65D51ED480CE0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> width =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Indique le pourcentage de la largeur utilisable du périphérique comme largeur d’image. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> heipercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Indique le pourcentage de la hauteur utilisable du périphérique comme hauteur d’image. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> sizepercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Indique le pourcentage de la propriété Memory Limit Embedded Media du périphérique pour limiter la taille de réponse à. Cela ne s’applique qu’aux réponses jpg. La qualité de l’image sera réduite jusqu’à ce que la taille de la réponse soit comprise dans le pourcentage spécifié. </p></td> 
 </tr> 
</table>

## Limite de mémoire d’image incorporée {#section-52f7c69ed8a341ceabf92ceee19b0f36}

Si la taille des images pouvant être incorporées sur une page Web est limitée au périphérique, la taille de l’image est limitée à cette taille tant que le format de réponse est jpg. Le proxy limite les réponses à 500 Mo si le périphérique n&#39;a pas de limite.

## Traitement principal {#section-bdf7c294b6824de9969c97fc1f8aa6d3}

Le proxy télécharge, vérifie et charge le fichier de données Device Atlas une fois par jour. La vérification extrait différentes propriétés pour différents périphériques et les compare aux valeurs attendues avant d’accepter les nouvelles données.
