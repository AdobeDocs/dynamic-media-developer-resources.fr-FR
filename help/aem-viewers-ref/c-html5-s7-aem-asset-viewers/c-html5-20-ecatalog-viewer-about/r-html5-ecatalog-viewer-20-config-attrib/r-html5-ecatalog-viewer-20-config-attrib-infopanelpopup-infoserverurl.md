---
title: InfoPanelPopup.infoServerUrl
description: InfoPanelPopup.infoServerUrl
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 83abaecb-cc85-4918-98ed-2770b4ca407b
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 2%

---

# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

`[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`URL du serveur d’infos`*`

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> URL du serveur d’infos</span></span> </p> </td> 
   <td> <p>Le modèle d’URL du serveur d’informations est utilisé pour récupérer les paires clé/valeur pour la substitution de variable dans le modèle de contenu du panneau d’informations. Le modèle spécifié contient généralement des espaces réservés aux macros qui sont remplacés par les données réelles avant que la demande ne soit envoyée au serveur. </p> <p><span class="codeph">$1$</span> est remplacé par la valeur de survol qui a déclenché l’activation de la fenêtre contextuelle <span class="codeph"></span> InfoPanel. </p> <p><span class="codeph"> $2$</span> est remplacé par le numéro de séquence de l’image actuelle dans la visionneuse d’images. </p> <p><span class="codeph"> $3$</span> est remplacé par le premier élément de chemin spécifié dans le nom de l’ensemble parent de l’élément actif. Il correspond généralement à l’ID du catalogue. </p> <p><span class="codeph"> $4$</span> est remplacé par l’élément suivant dans le chemin et correspond à l’ID de l’actif. La syntaxe réelle de la demande du serveur d’informations dépend du serveur d’informations et diffère d’un serveur à l’autre. Par exemple, voici un modèle standard de demande de serveur d’informations Dynamic Media : </p> <p><span class="codeph"> http ://server_domain/s7info/s7/$3$/$4$/$1$ (en anglais)</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Lorsque vous configurez la fenêtre contextuelle du panneau d’informations, le code HTML et le code JavaScript transmis au panneau d’informations s’exécutent sur l’ordinateur du client. Par conséquent, assurez-vous que ce code HTML et JavaScript code sont sécurisés.

## Propriétés {#section-71356e3c13244e62b0582980d9d05328}

Facultatif.

## Par défaut {#section-22e9af803f724434807d34e200eb7518}

Aucune

## Exemple {#section-4f70fa4705c54452893c72c9da7e998a}

`infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`
