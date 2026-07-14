---
description: InfoPanelPopup.infoServerUrl
solution: Experience Manager
title: InfoPanelPopup.infoServerUrl
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: f4bb0087-1e49-47e2-84b4-44b92fade36a
TQID: 'https://experienceleague.adobe.com/en4zktUgJGVG-e0fahRGTxasP3CVxhgfie6d0e3q6r4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 939895a2a379b02e733e48932434433bfa9663e1
workflow-type: tm+mt
source-wordcount: 198
ht-degree: 2%

---

# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

[!DNL `[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`]

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>Le modèle d’URL du serveur d’informations est utilisé pour récupérer les paires clé/valeur pour la substitution de variable dans le modèle de contenu du panneau informations. Le modèle spécifié contient généralement des espaces réservés de macro qui sont remplacés par les données réelles avant l’envoi de la requête au serveur. </p> <p><span class="codeph"> $1$</span> est remplacé par la valeur de survol qui a déclenché l’activation de <span class="codeph"> InfoPanelPopup</span>. </p> <p><span class="codeph"> $2$</span> est remplacé par le numéro de séquence de l’image actuelle dans la visionneuse d’images. </p> <p><span class="codeph"> $3$</span> est remplacé par le premier élément de chemin spécifié dans le nom de l'ensemble parent de l'élément actif. Il correspond généralement à l’identifiant du catalogue. </p> <p><span class="codeph"> $4$</span> est remplacé par l’élément suivant dans le chemin et correspond à l’identifiant de la ressource. La syntaxe réelle de la requête du serveur d'informations dépend du serveur d'informations et diffère d'un serveur à l'autre. Par exemple, voici un modèle de requête de serveur d’informations Dynamic Media type : </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Gardez à l’esprit que lorsque vous configurez la fenêtre contextuelle du panneau d’informations, le code HTML et le code JavaScript transmis au panneau d’informations s’exécutent sur l’ordinateur du client. Par conséquent, assurez-vous que ces codes HTML et JavaScript sont sécurisés.

## Propriétés {#section-71356e3c13244e62b0582980d9d05328}

Facultatif.

## Par défaut {#section-22e9af803f724434807d34e200eb7518}

Aucune

## Exemple {#section-4f70fa4705c54452893c72c9da7e998a}

[!DNL `infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`]
