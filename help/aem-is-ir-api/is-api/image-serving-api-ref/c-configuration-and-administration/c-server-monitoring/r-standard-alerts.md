---
description: Les alertes standard sont envoyées avec un message électronique consolidé à la fin de l’intervalle de moyenne configuré.
solution: Experience Manager
title: Alertes standard
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin,User
exl-id: eb691988-9f03-463f-bed5-2c230431f537
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# Alertes standard{#standard-alerts}

Les alertes standard sont envoyées avec un message électronique consolidé à la fin de l’intervalle de moyenne configuré.

Le tableau suivant décrit chaque type d’alerte standard.

<table id="table_02611F1B920E48A6973BFA969CA564EB"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Type d’alerte</b> </th> 
   <th class="entry"> <b>ID de titre</b> </th> 
   <th class="entry"> <b>Description</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>Requête verrouillée </p> </td> 
   <td> <p>Verrouiller </p> </td> 
   <td> <p>Envoyé lorsqu’une requête ne parvient pas à renvoyer une réponse au client dans les limites spécifiées. Peut être un indicateur de requêtes suspendues, ce qui peut entraîner l’épuisement du pool de threads Java. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Concurrence élevée </p> </td> 
   <td> <p>Conc </p> </td> 
   <td> Émis lorsque le nombre de requêtes qui sont traitées simultanément (le <i>chevauchement</i>) dépasse le seuil spécifié. Peut indiquer une condition de surcharge du serveur. </td> 
  </tr> 
  <tr> 
   <td> <p>Trafic minimal </p> </td> 
   <td> <p>Traf </p> </td> 
   <td> <p>Générée lorsque le taux de requête global est inférieur au seuil spécifié. Indique généralement un problème de communication avec le serveur (par exemple, lorsqu’un serveur est hors ligne). </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Taux d’erreur </p> </td> 
   <td> <p>Erreur </p> </td> 
   <td> <p>Émis lorsque le taux moyen de réponses d’erreur HTTP au cours de l’intervalle d’échantillonnage dépasse le seuil spécifié. Peut indiquer des problèmes de configuration, des images manquantes, des erreurs de programmation de site web ou de base de données. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Temps de réponse </p> </td> 
   <td> <p>RTime </p> </td> 
   <td> <p>Envoyé lorsque la durée moyenne de traitement des demandes au cours de l’intervalle d’échantillonnage dépasse le seuil spécifié. Indique généralement une condition de surcharge temporaire ou persistante du serveur ou du système de stockage d’images principal. </p> <p>Les réponses d’erreur ne sont pas prises en compte lors du calcul du temps de réponse moyen. </p> </td> 
  </tr> 
 </tbody> 
</table>
