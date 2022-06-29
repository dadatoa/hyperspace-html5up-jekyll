# hyperspace-html5up-jekyll

Il s'agit d'une adaptation du thème [html5up](https://html5up.net/) hyperspace ([demo ici](https://html5up.net/hyperspace)) pour Jekyll.

## 1. Utiliser ce thème/site

La méthode la plus simple est de cloner le projet, de faire les modifications necessaires, et déployer. Attention cependant: c'est un projet en cours de développement, il reste pas mal de choses à améliorer et il peut subsister des bugs. le thème d'origine est sous Creative Commons, n'oubliez pas de citer l'origine du thème si vous ne voulez pas vous facher avec son auteur.

Le repository possède une branche `gh-pages`, du coup, s'il est forké sur Github, Github Pages sera activé automatiquement sur la branche `gh-pages`. 

## 2. Landing page

La configuration de la landing page se fait via le fichier `_config.yml` et le fichicher `index.md`. 

### _config.yml

Les infos à personnaliser sont :

  - `title` : le titre du site
  - `description` : une description qui sera affichée en intro à la landing page et qui servira aussi pour la SEO via le plugin jekyll-seo-tag
  - `contacts` : contient les information de contact que vous souhaitez indiquer. Ces informations seront reprises dans la dernière section de la landing page, à `get in touch`
  - le cas échéant, il est possible d'ajouter une ligne `url` et une ligne `baseurl` pour spécifier l'écriture des urls dans les liens du site par Jekyll, c'est utile notemment si vous utiliser Github Pages pour l'hébergement
  
### index.md

Le gros de la configuration se passe dans le Front Matter du `index.md`. La page se divise en 4 section avec un menu qui permet de naviguer d'une section à l'autre. Chaque section a un certain nombre d'informations :

  - `title`: référence de la section dans le menu de navigation de la landing page
  
  - `id` : servent de point d'ancrage des sections de la page. De base, les ids dans le thème d'origine s'appellent `intro`, `one`, `two`et `three`, j'ai donc gardé ces reférence.
  
  - `template`, `color-style`, `animate` : définissent des classes sur les balises html nécessaires à la présentation des sections. 
  
    * `template` : a 5 possibilités :
      * `template: intro` : pour l'intro (section id `intro`)
      * `template: posts-list` : pour la liste de posts, par défaut section id `one`
      * `template: features-list` : pour la liste de pages, par défaut section id `two`
      * `template: follow-me` : pour afficher un bouton email et des contacts réseaux sociaux, par défaut section id `three`
      * `template: contact-form` : alternative à follow-me, affiche un formulaire de contact (à personnaliser et connecter à une API ou une base de données)
      
    * `color-style` : 3 possibilités :
      * `color-style: style1`
      * `color-style: style2`
      * `color-style: style3`
    
    * `animate` : défini le style d'animation pour l'apparition des éléments lors du lazy loading. 2 possibilités:
      * `animate: spotlights`
      * `animate: fade-up`
      
  - `descritpion` : facultatif, ajoute un descriptif (intro) à la section
  
 Ensuite, en fonction du template choisi, il est possible (voire nécessaire) de préciser des carractéristiques supplémentaires :
  
  - `template: posts-list` :
    * `source: posts` : comme c'est une liste, le template a besoin d'une source. J'y ai mis `posts` puisque c'est une collection pré-définie par Jekyll
    * `posts-limit: 3` : j'ai mis une limite au nombre de posts affichés sur la landing page, afin  qu'a mesure que le site grossi on ne se retrouve pas avec une page infinie! Le chiffre est abritraire, il est possible de mettre le chiffre qu'on veut, c'est une limite.
    
  - `template: features-list` : c'est une liste qui a besoin d'une source de données également, et comme pour les posts, je me suis appuyé sur une collection Jekyll existante : pages. De ce fait, toutes les pages ayant un titre seront représenté dans la section ayant pour template features-list.
  
## 3. Les layouts

Pour le reste du site, j'utilise 2 layouts : page et list. 

### `page`

Le layout `page` affiche un contenu statique, il peut être utiliser sur les posts et les pages. Les front matters des éléments qui ont le layout post peuvent contenir la source d'une image thumbnail et d'une image d'illustration (plus grosse). L'affichage des pages sur la landing page présente une icone, ce sont des icones font awesome et il suffit d'en indiqué le nom dans le front matter: `icon: cog` par exemple.

### `list`

Le layout `list` présente une liste d'éléments. Il est utilisé notemment pour la page blog qui affiche la liste des posts. Pour être fonctionnel, il a besoin d'une donnée particulière dans le front-matter : `source` (exemple: `source: posts`). En effet, s'agissant d'une liste, le layout à besoin de savoir quoi lister.

## 4. Le menu

Le menu affiche automatiquement, comme pour beaucoup de thème Jekyll, la liste des pages du site Jekyll qui contienne un élément de type `title`. Donc pour ajouter un élément au menu, il suffit de créer une page qui possède un `title`dans son front matter.

## Un exemple

Le repository possède une page Github Pages visible ici : (https://dadatoa.github.io/hyperspace-html5up-jekyll/)
