---
templateKey: blog-post
title: "Création d'un Blog avec CMS : un Deuxième Projet"
date: 2020-05-29T09:35:44.280Z
description: "Ma méthode de création: les étapes"
featuredpost: true
featuredimage: /img/idea.jpeg
tags:
  - article
  - blog
  - CMS
  - React
---
## Trouver un Bon Design

Comme je me le dis toujours, on ne va pas réinventer la roue et il y a déjà énormément de design disponibles sur la toile. Pour ma part, j'ai choisi <https://webflow.com/>. Il est possible d'y effectuer des recherches grâce à cette page <https://showcasesearch.webflow.io/>.
Il y a également cette page qui semble être une mine de ressources utiles:
<https://www.flowbase.co/>

Une fois un bon design choisi, il est temps d'en extraire le code source.

## Extraction du Code Source

### Extraire la Source HTML

Rien de plus simple. Une fois le site déployé, on peut extraire les fichiers **HTML** correspondant aux pages un par un grace au navigateur. S'il y a besoin de le développer, le raccourci de **VSCode** est `ALT-SHIFT-F` .



### Extraire la Source CSS

La aussi, pas trop compliqué. On peut soit utiliser le plugin **Chrome** **CSSused**, ou il est encore possible que le fichier **CSS** soit spécifié dans la tête du projet. S'il était nécessaire d'avoir plusieurs fichiers **CSS** et que l'on souhaite les restreindre à certains composants de l'application, on peut utiliser les **CSS modules**, apparemment directement avec **React 2**.

## Convertir les Pages Extraites en une Application React

Une brève analyse du code me permet de déterminer quels sont les composants que je dois extraire, potentiellement avec un peu de code supplémentaire. Ensuite, je signale tous les composants dans le code **HTML** en ajoutant l'attribut **data-component="nomDuComposant"**.
Puis, il me faut extraire ces composants pour chaque fichier **HTML** avec react-to-html. La commande a passer est **html2react "nomDuFichier.html"**.
S'ensuit un travail de montage avec **create-react-app et react-router-dom**, en incluant le **HTML** ainsi que le **CSS**.

## Relier l'Application à un CMS

C'est là un tout nouveau chapitre. Pour cela, il faut utiliser un headless CMS. Il y en a des tas. Voilà un article qui détaille cela:
<https://www.smashingmagazine.com/2020/04/web-app-headless-cms-react/>
Je vais essayer d'inclure mon projet à GraphCMS en suivant les conseils de cet article pour voir comment ça marche. Il y a aussi les bases de GraphQL que je dois continuer à apprendre avec le NetNinja...
<https://www.youtube.com/playlist?list=PL4cUxeGkcC9iK6Qhn-QLcXCXPQUov1U7f>
La réponse est donc une nouvelle technologie à apprendre: GraphQL!