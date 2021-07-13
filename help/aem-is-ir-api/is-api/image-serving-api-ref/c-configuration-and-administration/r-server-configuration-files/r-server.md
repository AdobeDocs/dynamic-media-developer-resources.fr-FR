---
description: Contient les paramètres du serveur de plateforme.
solution: Experience Manager
title: server.xml
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: 72b343ba-0d4b-405a-ace3-d44c4d4c44b0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 0%

---

# server.xml{#server-xml}

Contient les paramètres du serveur de plateforme.

Lors de la modification de ce fichier XML, veillez à conserver une syntaxe XML valide, faute de quoi le serveur Platform risque de ne pas démarrer.

Pour que les modifications soient prises en compte, le serveur Platform doit être redémarré après avoir modifié ce fichier.

Le diagramme suivant illustre les paramètres qui peuvent être modifiés dans ce fichier. Reportez-vous aux sections correspondantes plus tôt dans ce document pour une description de ces paramètres. Notez que ce diagramme n’est pas une représentation complète de [!DNL server.xml].

```
<Server>
   <Service name="Catalina">
     <Connector port="TC::PsPort" />
     <Connector port="TC::SslPort"
        keystoreFile="TC::keystoreFile"
        keystoreType="TC::keystoreType"
        keystorePass="TC::keystorePass" 
        scheme="https" secure="true" URIEncoding="UTF-8" />
     <Engine>
        <Valve directory="TC::directory" 
           maxDays="TC::maxDays" 
           prefix="TC::prefix" 
           pattern="TC::pattern" 
     </Engine>  
   </Service>
</Server>
```
