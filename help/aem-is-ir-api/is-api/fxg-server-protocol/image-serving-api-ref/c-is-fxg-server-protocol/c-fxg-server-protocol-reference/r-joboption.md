---
description: Appliquez les options de la tâche PDF. Un fichier d’options de tâche ou un paramètre prédéfini de PDF est un fichier généré par Illustrator dans la boîte de dialogue Options d’enregistrement en tant que PDF ou Paramètres prédéfinis de PDF dans InDesign.
solution: Experience Manager
title: joboption
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8e7224e7-d801-4550-b95e-24d15734043a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 38%

---

# joboption{#joboption}

Appliquez les options de la tâche PDF. Un fichier d’options de tâche ou un paramètre prédéfini de PDF est un fichier généré par Illustrator dans la boîte de dialogue Options d’enregistrement en tant que PDF ou Paramètres prédéfinis de PDF dans InDesign.

` joboption= *`value`*`

<table id="simpletable_BA7B58BE0B0740298D45DDEBE7832D93"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> valeur</span></span> </p> </td> 
  <td class="stentry"> <p>IPSID du fichier d’options de tâche. </p></td> 
 </tr> 
</table>

Le fichier d’options de tâche peut être chargé et publié via IPS/Dynamic Media Classic. Les options PDF contenues dans le fichier d’options de tâche sont utilisées lors de la génération du PDF.

Les options suivantes sont actuellement prises en charge :

<table id="simpletable_7E0AE8A06AE54A02AF0107FBEDF73D61"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Généraux </p></td> 
  <td class="stentry"> <p> Compatibilité </p> <p> Compression de niveau objet </p> <p> Incorporer les vignettes </p> <p> Optimiser pour l’affichage rapide des pages Web </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Images </p></td> 
  <td class="stentry"> <p> Sous-échantillon, Résolution, Seuil et Compression pour la couleur, le gris et le mono </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Polices </p></td> 
  <td class="stentry"> <p> Incorporer toutes les polices </p> <p> Incorporer les polices OpenType </p> <p> Jeux partiels de polices lorsque le pourcentage de caractères est inférieur à : </p> <p> Liste Toujours incorporer </p> <p> Liste Ne jamais incorporer </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Couleur </p></td> 
  <td class="stentry"> <p> Stratégie des couleurs (les images balisées uniquement sont traitées comme tout baliser) </p> <p> Mode de rendu du document </p> <p> Seuls les espaces de travail suivants sont pris en charge dans la version 4.2.5. </p> <p> 
    <ul id="ul_3F3EFDFB6A3340978AE31DEDF0FDA2C8"> 
     <li id="li_17A9FA99D6CA4C5182E383A85F0E3C90"> RVB <p> 
       <ul id="ul_1DD0C264DA1248319E751ADD18140C6D"> 
        <li id="li_B91B4D0C1D80442EB8690933AFA1F093"> e-sRGB </li> 
        <li id="li_D7F8C500DF5E4CBC8FFA4FEFB8E4E036"> scRGB avec gamme de codage [-4.0, 4.0] </li> 
        <li id="li_942CD69732984E16A71C2F75EC5B5245"> Lab D50 </li> 
        <li id="li_7063B9E98D1E4946AC8F0EF7BC988806"> PCS XYZ </li> 
        <li id="li_5809447576B147B68630C4B7EC2E7870"> Flat XYZ </li> 
        <li id="li_3B5DA42A04124A6BAA12343AFC19F620">Linear ROMM-RGB </li> 
        <li id="li_DEC3028FA9C34176B761D12B7179B44F">ROMM-RGB </li> 
        <li id="li_3E7E7C4A680C4E3EADE0A26048ECF1F4"> sYCC 8-bit </li> 
        <li id="li_16A615C9A74D443AB3C63B3FE3AB5443"> e-sYCC 8-bit </li> 
       </ul> </p> </li> 
     <li id="li_AFA6D4D8C0624AA495E2EB2F0F0C7F7B">Gris <p> 
       <ul id="ul_945389DD426F44C09EB9C7F23933CB77"> 
        <li id="li_DB0AE3DFFC184480BB91666FF1BB4776">Gray Gamma 1.8 </li> 
        <li id="li_755C556ED94740D1BD30EBE67018E074">Gray Gamma 2.2 </li> 
        <li id="li_67437440AFB54B7686333A55233AA87F">Dot Gain 10% </li> 
        <li id="li_0D6CA6004EC84048B5F2198406F4F343">Dot Gain 15% </li> 
        <li id="li_1AFD11C23AB147978559D8F00BFB3142">Dot Gain 20% </li> 
        <li id="li_6CD5ACEF6B0B49E8BACA8264FE0E9C44"> Dot Gain 25% </li> 
        <li id="li_AB5F1FA7111041BD82353E02A284A546">Dot Gain 30% </li> 
        <li id="li_7433278AE8054AD28BD38A0A6E4EF7EF"> sGray </li> 
       </ul> </p> </li> 
    </ul> </p> <p> Conserver les valeurs CMJN pour les espaces colorimétriques CMJN étalonnés </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Avancés </p></td> 
  <td class="stentry"> <p>L’option Conserver les commentaires OPI est toujours activée. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Normes </p></td> 
  <td class="stentry"> <p>Norme de conformité. </p></td> 
 </tr> 
</table>
