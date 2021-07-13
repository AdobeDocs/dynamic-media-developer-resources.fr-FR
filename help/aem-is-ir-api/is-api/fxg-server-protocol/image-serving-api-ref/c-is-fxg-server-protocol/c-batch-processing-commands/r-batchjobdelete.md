---
description: Supprimez la sortie d’une tâche.
solution: Experience Manager
title: batchjobdelete
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 9aca6693-32ac-4abd-9595-95bce60050ec
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 1%

---

# batchjobdelete{#batchjobdelete}

Supprimez la sortie d’une tâche.

Si une tâche est en cours d’exécution, elle est immédiatement arrêtée et toutes ses informations de traitement sont supprimées. Si la tâche s’est terminée correctement, son fichier de sortie est supprimé.

Ce paramètre :

<table id="simpletable_AACB976615FF4888A0816328DC48DCA3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> jobid</span> </p> </td> 
  <td class="stentry"> <p>Identifiant de tâche obtenu au moment de l’envoi. </p></td> 
 </tr> 
</table>

Renvoie :

État de la tâche au moment de la réception de la demande de suppression, erreur si `jobid` n’est pas valide ou si la tâche a déjà été supprimée.

## Exemple {#section-e0df8fc8e6554ba58e1fa937b8241ecf}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdelete&jobid=1005907604914d8eb63126b98f7172n76a5]
