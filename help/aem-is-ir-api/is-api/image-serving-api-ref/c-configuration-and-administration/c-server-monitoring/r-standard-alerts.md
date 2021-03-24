---
description: Les alertes standard sont envoyées avec un message électronique consolidé à la fin de l’intervalle de moyenne configuré.
solution: Experience Manager
title: Alertes standard
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%

---


# Alertes standard {#standard-alerts}

Les alertes standard sont envoyées avec un message électronique consolidé à la fin de l’intervalle de moyenne configuré.

Le tableau suivant décrit chaque type d’alerte standard.

<table id="table_02611F1B920E48A6973BFA969CA564EB"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Type d'alerte</b> </th> 
   <th class="entry"> <b>ID de titre</b> </th> 
   <th class="entry"> <b>Description</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>Requête verrouillée </p> </td> 
   <td> <p>Verrouiller </p> </td> 
   <td> <p>Envoyé lorsqu’une requête ne parvient pas à renvoyer une réponse au client dans le délai spécifié. Peut être un indicateur de requêtes suspendues, ce qui peut entraîner une épuisement du pool de threads Java. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Concurrence élevée </p> </td> 
   <td> <p>Conc </p> </td> 
   <td> Émis lorsque le nombre de requêtes traitées simultanément (le <i>chevauchement</i>) dépasse le seuil spécifié. Peut indiquer une situation de surcharge du serveur. </td> 
  </tr> 
  <tr> 
   <td> <p>Trafic minimal </p> </td> 
   <td> <p>Traf </p> </td> 
   <td> <p>Généré lorsque le taux de demande global est inférieur au seuil spécifié. Indique généralement un problème de communication avec le serveur (par exemple, lorsqu’un serveur est hors ligne). </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Taux d’erreurs </p> </td> 
   <td> <p>Erreur </p> </td> 
   <td> <p>Émis lorsque le taux moyen de réponses d’erreur HTTP au cours de l’intervalle d’échantillonnage dépasse le seuil spécifié. Peut indiquer des problèmes de configuration, des images manquantes, des erreurs de programmation de site Web ou de base de données. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Temps de réponse </p> </td> 
   <td> <p>RTime </p> </td> 
   <td> <p>Envoyé lorsque la durée moyenne de traitement de la demande au cours de l’intervalle d’échantillonnage dépasse le seuil spécifié. Indique généralement une situation de surcharge temporaire ou persistante du serveur ou du système d’enregistrement d’images principal. </p> <p>Les réponses aux erreurs ne sont pas prises en compte lors du calcul du temps de réponse moyen. </p> </td> 
  </tr> 
 </tbody> 
</table>

