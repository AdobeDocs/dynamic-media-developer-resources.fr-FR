---
description: Décrit les paramètres d’opération communs gérés par l’API du service Web IPS.
solution: Experience Manager
title: Méthodes d’exploitation
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 020c8e63-ad4e-4c0d-8da6-b51efb2b89a5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 0%

---

# Méthodes d’exploitation{#operations-methods}

Cette section décrit les paramètres d’opération communs gérés par l’API du service Web IPS.

Pour une description complète de chaque paramètre d’opération, voir [Paramètres d’opération](/help/aem-ips-api/operations/c-operations-intro/c-methods/c-methods.md).

## Handles : À propos {#section-094ce1afa6244fa5b2c762f44ffdca1c}

Gère les objets IPS de référence renvoyés par certaines opérations API. Vous pouvez également transmettre des poignées en tant que paramètres aux appels d’opération suivants. Les gestionnaires sont des types de données de chaîne ( `xsd:string`).

Les gestionnaires ne sont destinés qu’à une seule session d’application. En outre, vous devez rendre les gestionnaires persistants, car leur format peut changer entre les versions d’IPS. Lorsque vous écrivez des applications interactives, vous implémentez des délais d’expiration de session et ignorez toutes les poignées entre les sessions, en particulier après une mise à niveau d’IPS. Lorsque vous écrivez des applications non interactives, appelez les opérations appropriées pour récupérer les poignées à chaque exécution de l’application. Les exemples de code Java/Axis2 suivants présentent une exécution de code correcte et incorrecte :

**Code de gestion incorrect**

Cet exemple de code est incorrect car il contient une valeur codée en dur (555) pour le nom d’entreprise.

```
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle("555");// INCORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

**Correct Handle Code**

Cet exemple de code est correct, car il appelle `getCompanyInfo` pour renvoyer un gestionnaire valide. Elle ne repose pas sur une valeur codée en dur. Utilisez cette méthode ou une autre API IPS équivalente pour renvoyer la poignée requise.

```
GetCompanyInfoParam companyInfoParam = new GetCompanyInfoParam(); 
companyInfoParam.setCompanyName("My Company"); GetCompanyInfoReturn companyInfoReturn = ipsApi.getCompanyInfo(companyInfoParam, authHeader); 
String companyHandle = companyInfoReturn.getCompanyInfo().getCompanyHandle(); 
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle(companyHandle); //CORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

## Types de gestion courants {#section-e683ac8283284f9688e63f51a494f7a0}

**companyHandle**

La plupart des opérations nécessitent que vous définissiez un contexte d’entreprise en transmettant un paramètre `companyHandle`. Le gestionnaire de la société est un pointeur renvoyé par certaines opérations telles que `getCompanyInfo`, `addCompany` et `getCompanyMembership`.

**userHandle**

Le paramètre `userHandle` est un paramètre facultatif pour les opérations qui ciblent un utilisateur spécifique. Par défaut, ces opérations ciblent l’utilisateur appelant (l’utilisateur dont les informations d’identification sont transmises pour authentification). Toutefois, les utilisateurs administrateurs disposant des autorisations appropriées peuvent spécifier un autre utilisateur. Par exemple, l’opération `setPassword` définit normalement le mot de passe de l’utilisateur authentifié, mais un administrateur peut utiliser le paramètre `userHandle` pour définir le mot de passe d’un autre utilisateur.

Pour les opérations qui nécessitent un contexte d’entreprise (à l’aide du paramètre `companyHandle` ), les utilisateurs authentifiés et les utilisateurs cibles doivent être membres de la société spécifiée. Pour les opérations qui ne nécessitent pas de contexte d’entreprise, les utilisateurs authentifiés et ciblés doivent tous deux appartenir à au moins une société commune.

Les opérations suivantes peuvent récupérer les noms d’utilisateur :

* `getUsers`
* `getAllUsers`
* `getUserInfo`
* `getCompanyMembers`
* `getGroupMembers`
* `addUser`

**accessUserHandle et accessGroupHandle**

Par défaut, les opérations qui nécessitent des autorisations d’accès (lecture, écriture, suppression) fonctionnent dans le contexte des autorisations de l’utilisateur appelant. Certaines opérations vous permettent de modifier ce contexte avec le paramètre `accessUserHandle` ou `accessGroupHandle` . Le paramètre `accessUserHandle` permet à un administrateur d’emprunter l’identité d’un autre utilisateur. Le paramètre `accessGroupHandle` permet à l’appelant de fonctionner dans le contexte d’un groupe d’utilisateurs spécifique.

**responseFieldArray et excludeFieldArray**

Certaines opérations permettent à l’appelant de restreindre les champs inclus dans la réponse. La limitation des champs peut contribuer à réduire le temps et la mémoire nécessaires au traitement de la requête et à réduire la taille des données de réponse. L’appelant peut demander une liste spécifique de champs en transmettant un paramètre `responseFieldArray` ou avec une liste énumérée de champs exclus au moyen du paramètre `excludeFieldArray` .

`responseFieldArray` et `excludeFieldArray` spécifient des champs à l’aide d’un chemin de noeud séparé par `/`. Par exemple, pour indiquer que `searchAssets` renvoie uniquement le nom, la date de dernière modification et les métadonnées de chaque ressource, reportez-vous aux éléments suivants :

```
<responseFieldArray> 
   <items>assetArray/items/name</items> 
   <items>assetArray/items/lastModified</items> 
   <items>assetArray/items/metadataArray</items> 
</responseFieldArray>
```

De même, pour renvoyer tous les champs (sauf les autorisations) :

```
<excludeFieldArray> 
   <items>assetArray/items/permissions</items> 
</excludeFieldArray>
```

Notez que les chemins d’accès au noeud sont relatifs à la racine du noeud de retour. Si vous spécifiez un champ de type complexe sans aucun de ses sous-éléments (par exemple, `assetArray/items/imageInfo`), tous ses sous-éléments sont inclus. Si vous spécifiez un ou plusieurs sous-éléments dans un champ de type complexe (par exemple, `assetArray/items/imageInfo/originalPath`), seuls ces sous-éléments sont inclus.

Si vous n’incluez pas `responseFieldArray` ou `excludeFieldArray` dans une requête, tous les champs sont renvoyés.

**Locale**

Depuis IPS 4.0, l’API IPS prend en charge la définition du contexte de paramètres régionaux d’une opération en transmettant le paramètre de paramètres régionaux `authHeader`. Si le paramètre régional n’est pas présent, l’en-tête HTTP `Accept-Language` est utilisé. Si cet en-tête n’est pas non plus présent, le paramètre régional par défaut du serveur IPS est utilisé.

Certaines opérations utilisent également des paramètres régionaux explicites, qui peuvent différer du contexte des paramètres régionaux de l’opération. Par exemple, l’opération `submitJob` utilise un paramètre `locale` qui définit les paramètres régionaux utilisés pour la journalisation des tâches et la notification électronique.

Les paramètres régionaux utilisent le format `<language_code>[-<country_code>]`

Si le code de langue est un code à deux lettres minuscule spécifié par la norme ISO-639 et que le code de pays facultatif est un code à deux lettres majuscules spécifié par la norme ISO-3266. Par exemple, la chaîne du paramètre régional pour l’anglais américain est `en-US`.
