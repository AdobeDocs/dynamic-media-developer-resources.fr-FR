---
description: Paramètres contribuant à améliorer la netteté des images pour les fichiers pyramid TIF optimisés.
solution: Experience Manager
title: UnsharpMaskOptions
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 7150b4a8-a44d-4858-96f2-6004d5f48e77
TQID: 'https://experienceleague.adobe.com/J9LoVO0ZOapo0ao5gJoyNXc5qu3A3fNDD8ALRAiHudg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 205
ht-degree: 9%

---

# [!DNL UnsharpMaskOptions]{#unsharpmaskoptions}

Paramètres contribuant à améliorer la netteté des images pour les fichiers pyramid TIF optimisés.

`unsharpMaskOptions=[ *`quantité, rayon, seuil, monochrome`*]`

## Paramètres {#section-c3f0d03136ba4422819cb463bd393885}

Spécifiez une valeur pour `unsharpMaskOptions` options avec `minOccurs=" *`n`*".`

<table id="table_D1392963C5694969A9D546F82DB6F45C">
 <thead>
  <tr>
   <th colname="col1" class="entry"> Nom </th>
   <th colname="col2" class="entry"> Type </th>
   <th colname="col3" class="entry"> Description </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> montant</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:double</span></td>
   <td colname="col3"><p>Contrôle le contraste appliqué aux pixels de contour. 
     <ul id="ul_7AA17E354EE64BC4A5BEAE853FF17191">
      <li id="li_42FB21C7ED884E1DB03274130B8DCB10">Plage : 0,0 - 5,0 </li>
      <li id="li_E980CAA1A9C54D60A121F21C964820FF">Valeur par défaut : 0 </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> rayon</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:double</span></td>
   <td colname="col3"><p>Contrôle la netteté en définissant le nombre de pixels autour du bord d’une image. La valeur appropriée dépend de la taille de l’image. 
     <ul id="ul_D4391CD407DE4B48AF4523EBD85D0D40">
      <li id="li_8AEF11A489484EFD91416F8A03C4DB25">Plage : 0,0 - 250,0 </li>
      <li id="li_9F1D1B52AFBA46B8BDCDF99A21140002">Les valeurs faibles accentuent uniquement les pixels de contour. </li>
      <li id="li_7D9FD8AA4899404283D7AB596364A4AF">Les valeurs élevées accentuent une bande plus large de pixels. </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> seuil</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:int</span></td>
   <td colname="col3"><p>Détermine l’écart recherché entre les pixels de la zone environnante avant qu’ils ne soient considérés comme des pixels de contour et ne puissent être accentués. 
     <ul id="ul_117E556E3ECF42CC878DD80D338D19CA">
      <li id="li_CFEE76DB78BF437E8463C9089486F8A6">Plage : 0 - 255 (entiers uniquement). </li>
      <li id="li_77113DC2698A4D48B11288718766E6A2">Valeur par défaut : 6 </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> monochrome</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:int</span></td>
   <td colname="col3"><p>Les valeurs incluent <span class="codeph"> 0</span> ou <span class="codeph"> 1</span> uniquement. </p><p>Définissez cette valeur sur <span class="codeph"> 0</span> pour appliquer séparément chaque composante de couleur ou sur <span class="codeph"> 1</span> pour appliquer uniquement la luminosité (intensité) de l’image. Le masque de calque ou le masque composite est également accentué . </p><p><span class="codeph"><span class="varname"> monochrome</span></span> est ignoré pour les images en niveaux de gris. </p></td>
  </tr>
 </tbody>
</table>

## Exemple {#section-38adca96c7714cfea35331d20403f59e}

```
<element name="unsharpMaskOptions" type="types:UnsharpMaskOptions" minOccurs="0"/>
    <complexType name="UnsharpMaskOptions">
        <sequence>
            <element name="amount" type="xsd:double" minOccurs="0"/>
            <element name="radius" type="xsd:double" minOccurs="0"/>
            <element name="threshold" type="xsd:int" minOccurs="0"/>
            <element name="monochrome" type="xsd:int" minOccurs="0"/>        
        </sequence>
    </complexType>
```

## Utilisé par {#section-db8124a5468b498694a780f8a56a4560}

Le type de `unsharpMaskOptions` est utilisé par :

* [RetraiterTâcheRessources](../../types/c-data-types/r-reprocess-assets-job.md#reference-a303f7832ae44fdab1dca7cc8bef3fa3)
* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)

>[!MORELIKETHIS]
>
>* [Référence de l’API du service d’images : op_usm](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-serving-api/image-serving-api/http-protocol-reference/command-reference/r-op-usm.html)
