---
description: Définit le mot de passe d’un utilisateur spécifique ou de l’utilisateur par défaut sur une valeur spécifique, selon que vous spécifiez ou non un nom d’utilisateur.
solution: Experience Manager
title: setPassword
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e8d95b55-0a97-4887-b711-7be99833c389
TQID: 'https://experienceleague.adobe.com/01-S0tkyxnXa6YT4Wch4SB5kPAcTo-ImUhN4uNUY3ks'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 230
ht-degree: 4%

---

# setPassword{#setpassword}

Définit le mot de passe d’un utilisateur spécifique ou de l’utilisateur par défaut sur une valeur spécifique, selon que vous spécifiez ou non un nom d’utilisateur.

La date d’expiration du mot de passe est facultative. En cas d’omission, le mot de passe n’expire jamais.

## Types d’utilisateurs autorisés {#section-39ae61d78cab4492a6efc1fc0d2f06c4}

>[!NOTE]
>
>*Uniquement* le type d’utilisateur `IpsAdmin` est autorisé à exécuter des appels setPassword sur d’autres utilisateurs.

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`

## Paramètres {#section-0531294341f7483d89dacaa393dd659a}

**Input (setPasswordParam)**

<table id="table_BF54512811344E0B979C5070354E8048"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nom </p> </th> 
   <th colname="col2" class="entry"> <p>Type </p> </th> 
   <th colname="col3" class="entry"> <p>Obligatoire </p> </th> 
   <th colname="col4" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> userHandle </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Handle utilisateur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mot de passe <span class="varname"> </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p>Mot de passe. </p> <p>Les exigences suivantes s’appliquent au mot de passe choisi : </p> <p> 
     <ul id="ul_E5BE3621127C476788412174584075B3"> 
      <li id="li_0132852AFD774659A0224C450F19418C">Les mots de passe respectent la casse. </li> 
      <li id="li_71224B3A89C8461AB689BAD383EC8CEA">La longueur minimale du mot de passe est de huit caractères. </li> 
      <li id="li_C21B6843EA734D1ABE0580185F775408">Le mot de passe doit contenir un ou plusieurs caractères des classes de caractères suivantes : 
       <ul id="ul_D5D3911AD6214035BBD2AB8350A459C7"> 
        <li id="li_6E3F084100104F2CBCF130EF8852C7B7">Caractères anglais minuscules. Par exemple, <span class="codeph"> a b c d e </span> etc </li> 
        <li id="li_1FDED8D7348842BC857320D797D41217">Caractères anglais en majuscule. Par exemple, <span class="codeph"> A B C D E </span> etc. </li> 
        <li id="li_C3C4D5412AA749F3B78F37B2B696CF80">Nombres. Par exemple, <span class="codeph"> 1 2 3 4 5 </span> etc. </li> 
        <li id="li_2730798F26E74B878BEDE510CD06D8DD">Caractères spéciaux. Par exemple, vous pouvez utiliser l’une des méthodes suivantes : <span class="codeph"> &grave; ~ ! @ # $ % ^ * ( ) _ + - = { } | [ ] &amp; \ : " ; ' &lt; &gt; ? , . / </span> </li> 
       </ul> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> passwordExpires </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:dateTime </span> </p> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Détermine la date d’expiration du mot de passe. <p>Remarque : indiquez le fuseau horaire avec la demande pour ce champ. Les fuseaux horaires sont adaptés à l’heure centrale. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (setPasswordReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-23a6fbabdb3c4c3180076057e47ae567}

Cet exemple de code crée un mot de passe utilisateur. Le mot de passe n’expire jamais, car `passwordExpires` a été omis.

**Requête**

```java
<ns1:setPasswordParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">  
   <ns1:userHandle>3341|juser@scene7.com</ns1:userHandle> 
   <ns1:password>@Do6e$ySt3mz</ns1:password> 
</ns1:setPasswordParam>
```

**Réponse**

Aucune
