---
title: en-tête
description: Élément d’en-tête de réponse HTTP. Facultatif dans <rule> les éléments.</rule>
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 40849602-16b2-471b-9128-14653e84a45a
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 2%

---

# en-tête{#header}

Élément d’en-tête de réponse HTTP. Facultatif dans les `<rule>` éléments.

## Attributs {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= « *text* »** : Obligatoire. Spécifie le nom de l’en-tête HTTP.

**`Action`= « set » |`"add"`**:Optionnel. La valeur par défaut est `"set"`, qui remplace toute valeur d’en-tête actuelle. Spécifiez `"add"` cette règle afin de pouvoir ajouter la valeur de l’en-tête séparée par une virgule.

## Données {#section-a387f541396c49d99c29692a38032914}

Valeur d’en-tête.

## Description {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

Permet d’ajouter de nouveaux en-têtes de réponse HTTP et d’ajouter ou de remplacer des valeurs d’en-têtes prédéfinis. Les noms et valeurs doivent être conformes aux normes HTTP. Aucun codage supplémentaire n’est appliqué.

Les variables de substitution Image Serving peuvent être utilisées dans le nom et la valeur de l’en-tête. Cela permet de contrôler les deux chaînes à partir de la demande.

## Exemple {#section-cb5b738b9b93407cb2f4d35af3e59c02}

La règle suivante applique un en-tête personnalisé lorsque la valeur d’en-tête est spécifiée dans la requête en tant que variable :

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

Cette règle est déclenchée par la requête suivante, définissant l’en-tête `Edge-Control::no-store`de réponse HTTP :

`http://server/is/image/cat/id?$Edge-Control=no-store`
