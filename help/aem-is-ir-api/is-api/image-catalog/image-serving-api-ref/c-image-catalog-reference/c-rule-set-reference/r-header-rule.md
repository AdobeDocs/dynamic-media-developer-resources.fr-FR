---
description: Elément d’en-tête de réponse HTTP. Facultatif dans les éléments <rule>.
solution: Experience Manager
title: en-tête
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 3%

---


# en-tête{#header}

Elément d’en-tête de réponse HTTP. Facultatif dans les éléments `<rule>`.

## Attributs {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*text*&quot;**  : Obligatoire. Indique le nom de l’en-tête HTTP.

**`Action`= &quot;set&quot; |`"add"`**: Facultatif. La valeur par défaut est `"set"`, ce qui remplace toute valeur d’en-tête active. Spécifiez `"add"` pour ajouter la valeur d’en-tête, en la séparant par une virgule.

## Données {#section-a387f541396c49d99c29692a38032914}

Valeur d’en-tête.

## Description {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

Permet d’ajouter de nouveaux en-têtes de réponse HTTP, ainsi que d’ajouter ou de remplacer des valeurs d’en-têtes prédéfinis. Les noms et valeurs doivent être conformes aux normes HTTP. Aucun codage supplémentaire ne sera appliqué.

Les variables de substitution Image Serving peuvent être utilisées dans le nom de l’en-tête et la valeur de l’en-tête. Cela permet de contrôler les deux chaînes de la requête.

## Exemple {#section-cb5b738b9b93407cb2f4d35af3e59c02}

La règle suivante applique un en-tête personnalisé lorsque la valeur d’en-tête est spécifiée dans la requête sous la forme d’une variable :

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

Cette règle est déclenchée par la requête suivante, en définissant l’en-tête de réponse HTTP `Edge-Control::no-store` :

`http://server/is/image/cat/id?$Edge-Control=no-store`
