---
description: InfoPanelPopup.template
solution: Experience Manager
title: InfoPanelPopup.template
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 3%

---


# InfoPanelPopup.template{#infopanelpopup-template}

`[InfoPanelPopup.|<containerId>_infoPanelPopup.]template= *`modèle`*`

<table id="table_A6B1B446A7AE4A4A8B552C07EC88E518"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> modèle</span></span> </p> </td> 
   <td> <p>Le modèle de contenu dans lequel les données renvoyées par le serveur d’informations sont fusionnées. </p> <p>Le modèle de contenu est un fichier XML suivant cette DTD : </p> <p> <code>&lt;!DOCTYPE&nbsp;info&nbsp;[
      &lt;!ELEMENT&nbsp;info&nbsp;(var&nbsp;#PCDATA)
      &lt;!ELEMENT&nbsp;var&nbsp;(#PCDATA)&gt;
      &lt;!ATTLIST&nbsp;var&nbsp;
      name&nbsp;CDATA&nbsp;#REQUIRED
      rollover&nbsp;CDATA&nbsp;#IMPLIED&nbsp;&gt;
      ]&gt;</code> </p> <p>La syntaxe réelle du modèle de contenu est la suivante : </p> <p> <code>&lt;info&gt;
      &lt;var&nbsp;name='VAR_NAME'&nbsp;rollover='ROLLOVER_KEY'&gt;&lt;!CDATA[&nbsp;VAR_VALUE&nbsp;]&gt;
      &lt;![CDATA[&nbsp;TEMPLATE_CONTENT&nbsp;]&gt;
      &lt;/info&gt;</code> </p> <p>En d’autres termes, le modèle doit être début avec l’élément <span class="codeph"> &lt;info&gt;</span> qui peut contenir des éléments facultatifs par défaut <span class="codeph"> &lt;var&gt;</span>. Le contenu du modèle lui-même, <span class="codeph"> TEMPLATE_CONTENT</span> est du texte HTML. En outre, le modèle de contenu peut contenir des noms de variable compris dans des caractères <span class="codeph"> $</span>. Ces caractères sont remplacés par les valeurs de variable renvoyées par le serveur d’informations ou par celles par défaut. </p> <p>Les variables par défaut définies dans le modèle peuvent être globales (si l’attribut de survol n’est pas défini) ou spécifiques à une certaine clé de survol (si l’attribut de survol est présent). </p> <p>Lors du traitement des modèles, les variables spécifiques aux clés de survol sont prioritaires sur les variables globales. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Notez que lorsque vous configurez la fenêtre contextuelle du panneau d’informations, le code HTML et le code JavaScript transmis au panneau d’informations s’exécutent sur l’ordinateur du client. Par conséquent, assurez-vous que ce code HTML et ce code JavaScript sont sécurisés.

## Propriétés {#section-6dd7785357d740d095fa9f7fd0f67da4}

Facultatif.

## Par défaut {#section-cd5db06d08aa4de49e37d6c938b41570}

Aucune

## Exemple {#section-16d184665c484964af9a22f79ff3f840}

En supposant que la réponse du serveur d’informations renvoie le nom du produit sous la forme de variable `$1$` et que l’URL de l’image du produit soit renvoyée sous la forme de variable `$2$`.

`template=<info><![CDATA[Product description:$1$<br>Product image:<img src="$2$">]]></info>`
