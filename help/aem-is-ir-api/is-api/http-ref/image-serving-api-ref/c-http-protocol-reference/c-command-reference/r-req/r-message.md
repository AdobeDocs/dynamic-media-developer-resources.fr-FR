---
description: Message client. Fournit un mécanisme permettant aux clients d'insérer des SMS courts dans le journal du serveur.
solution: Experience Manager
title: message
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 47e51181-714c-4b25-a375-f3b2238cd534
TQID: 'https://experienceleague.adobe.com/LmWXluV-uBCDX7ip4mUDsmlknIT8SPQmnF4aOYd89s8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 52
ht-degree: 3%

---

# message{#message}

Message client. Fournit un mécanisme permettant aux clients d&#39;insérer des SMS courts dans le journal du serveur.

`req=message&message= *`chaîne`*`

<table id="simpletable_9AF29AA336C4447BBC2FD4A7D43ED91B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> string</span> </p> </td> 
  <td class="stentry"> <p>Chaîne du message. </p></td> 
 </tr> 
</table>

La réponse HTTP ne peut pas être mise en cache. Une réponse vide est renvoyée avec le type MIME `text/plain`.
