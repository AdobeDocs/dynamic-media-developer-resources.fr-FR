---
description: Les alertes standard sont envoyées avec un e-mail consolidé à la fin de l’intervalle de calcul de la moyenne configuré.
solution: Experience Manager
title: Alertes standard
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: eb691988-9f03-463f-bed5-2c230431f537
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# Alertes standard{#standard-alerts}

Les alertes standard sont envoyées avec un e-mail consolidé à la fin de l’intervalle de calcul de la moyenne configuré.

Le tableau suivant décrit chaque type d’alerte standard.

<table id="table_02611F1B920E48A6973BFA969CA564EB"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Type d’alerte</b> </th> 
   <th class="entry"> <b>ID du titre</b> </th> 
   <th class="entry"> <b> Description </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>Demande verrouillée </p> </td> 
   <td> <p>Verrouiller </p> </td> 
   <td> <p>Envoyé lorsqu’une requête ne parvient pas à renvoyer une réponse au client dans les limites du seuil spécifié. Peut indiquer des requêtes bloquées, qui peuvent entraîner une déplétion du pool de threads Java. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Simultanéité élevée </p> </td> 
   <td> <p>Conc </p> </td> 
   <td> Émis lorsque le nombre de requêtes traitées simultanément (le <i>chevauchement</i>) dépasse le seuil spécifié. Peut indiquer une condition de surcharge du serveur. </td> 
  </tr> 
  <tr> 
   <td> <p>Trafic minimal </p> </td> 
   <td> <p>Traf </p> </td> 
   <td> <p>Généré lorsque le taux de requêtes global chute en dessous du seuil spécifié. Indique généralement un problème de communication du serveur (par exemple, lorsqu’un serveur est mis hors ligne). </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Taux d’erreurs </p> </td> 
   <td> <p>Erreur </p> </td> 
   <td> <p>Émis lorsque le taux moyen de réponses d’erreur HTTP pendant l’intervalle d’échantillonnage dépasse le seuil spécifié. Peut indiquer des problèmes de configuration, des images manquantes, des erreurs de programmation de site web ou de base de données. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Temps de réponse </p> </td> 
   <td> <p>RTime </p> </td> 
   <td> <p>Envoyé lorsque le temps de traitement moyen des requêtes au cours de l’intervalle d’échantillonnage dépasse le seuil spécifié. Indique généralement une condition de surcharge temporaire ou persistante du serveur ou du système de stockage d’images principal. </p> <p>Les réponses d’erreur ne sont pas prises en compte lors du calcul du temps de réponse moyen. </p> </td> 
  </tr> 
 </tbody> 
</table>
