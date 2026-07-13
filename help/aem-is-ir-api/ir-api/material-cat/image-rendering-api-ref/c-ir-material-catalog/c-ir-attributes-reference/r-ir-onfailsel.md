---
title: OnFailSel
description: Gestion des erreurs de sélection des prélèvements. Indique l’action à effectuer si la commande sel= échoue, car l’emplacement du pixel spécifié n’est pas dans la zone de masque d’un objet sélectionnable.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d5485569-def8-4e16-9f0e-7dd30d38439d
TQID: 'https://experienceleague.adobe.com/rgp6VEJFX8BCZF76fg-1xzrGTuAm87-9HgGHpkNLmtE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 118
ht-degree: 6%

---

# OnFailSel{#onfailsel}

Gestion des erreurs de sélection des prélèvements. Indique l’action à effectuer si la commande `sel=` échoue parce que l’emplacement du pixel spécifié n’est pas dans la zone de masque d’un objet sélectionnable.

## Propriétés {#section-cec491e6c5c744f9bfafaaa9d8774f83}

Énumération.

<table id="simpletable_1CFD2BC6F9BC4D2AB372EAF115B7F2FC"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Hériter de <span class="codeph"> valeur par défaut : OnFailSel </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Conserver la sélection précédente. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>Désélectionnez cette option ; toute tentative d'application d'un matériau ou d'affichage/masquage d'objets est ignorée. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Renvoyer une erreur. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>Sélectionnez le groupe par défaut (premier groupe de la hiérarchie de la vignette contenant les objets rendus). </p> </td> 
 </tr> 
</table>

## Par défaut {#section-c25f458f9f8f4236963a95779529e664}

Hérité de `default::OnFailSel` si non défini.

## Voir aussi {#section-f8b15dd64c674c5484d190dd9e3016af}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b) , [attribute::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)

