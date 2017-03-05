# Module 2 : le traitement scientométrique

L’objectif de ce module est d'aborder l'analyse scientométrique pour les publications CRISPR.

## Comprendre ce qu'est l'analyse scientométrique

En un mot, est appelé scientométrie toute analyse qui s'appuie sur des statistiques portant sur les méta-données de publication (nom de la revue, nom des auteurs, mot-clés, citation des articles) pour caractériser la connaissance sur un domaine, soit dans sa dimension congitive (les thématiques, la relation entre les articles), soit dans sa dimension sociale (qui travaille avec qui, etc.). Par statistiques, il faut entendre tout traitement de données : cela peut-être des comptages (nombre d'articles par années), des modèles compliqués (effet du genre sur le taux de publication) ou de l'analyse de réseaux (qui est connecté à qui).

Pour aller plus loin, si cela vous intéresse, vous trouverez plus d'information dans l'article de l'Encyclopédie :

> Leydesdorff, L., & Milojević, S. (2015). Scientometrics. International Encyclopedia of the Social & Behavioral Sciences (Second Edition), 322–327.

Ce faisant, la scientométrie (certains utilisent le terme de bibiométrie) s'appuie sur trois étapes différentes : lier une question de recherche avec les possibilités offertes par l'étude d'un corpus de données de publications scientifiques, construire ce corpus, l'analyser.

De nombreuses utilisations existent, que ce soit pour évaluer l'impact des politiques publiques dans un domaine ou pour cartographier l'ensemble des connaissances : http://www.mapofscience.com/. Pour avoir quelques idées de ce qu'il est possible de faire, vous pouvez jeter un coup d'oeil, mais sans vous étendre, à ces quelques articles :

La caractérisation d'un domaine de recherche :

> Raimbault, B., Cointet, J., & Joly, P.-B. (2013). Caractérisation du processus d’émergence de la biologie synthétique à partir d'une approche scientométrique. Medecine Sciences : M/S, 29 Spec No, 45–47. http://doi.org/10.1051/medsci/201329s213

Le profil de publication d'un chercheur :

> Gonzalez-Alcaide, G. (2014). Scientometric portrait of biochemist Santiago Grisolia: publication productivity, collaboration patterns, and citation analysis. Research Evaluation, 23(2), 150–165. http://doi.org/10.1093/reseval/rvu003

L'évolution dans le temps de thématiques d'un domaine

> Chavalarias, D., & Cointet, J. P. (2013). Phylomemetic Patterns in Science Evolution-The Rise and Fall of Scientific Fields. PLoS ONE, 8(2). http://doi.org/10.1371/journal.pone.0054847



## Application à partir de SCOPUS

Par la suite nous allons utiliser SCOPUS pour faire une première analyse de corpus. Nous allons pour le moment mettre un peu les mains dans les données sans pour autant poser des questions spécifiques : c'est la phase *exploratoire*.

1/ Identifiez l'article sur CRISPR le plus cité référencé dans SCOPUS sur CRISPR. Vérifiez si c'est aussi le cas dans Google Scholar. Utilisez ensuite dans SCOPUS l'onglet "Analyze search results" pour caractériser la dynamique des citations de cet article. En particulier : est-ce que l'article a été cité tout de suite ? Dans quels journaux principalement cet article est cité ? Quel est le principal domaine ? Quels sont les principaux pays des auteurs ? 

En faisant ça, vous commencez à produire des données statistiques décrivant un corpus particulier (ici, l'ensemble des publications référencées qui ont cité un article). On aurait envie d'aller un peu plus loin maintenant, non ?

## Faire une première visualisation

Souvent, dans la première phase d'une enquête, on a envie de voir des choses pour s'orienter et poser des questions plus précises. Il est souvent inutile de se lancer dans des questions précises quand on a pas une vision générale. Pour avoir cette vision générale, il existe des outils qui simplifient le travail. La contrepartie est que ces outils intègrent UNE approche particulière, et limitent ainsi les marges de liberté.

Je propose d'utiliser un de ces outils, développé par un laboratoire néérlandais (le CWTS) : WOSViewer. Il est écrit dans le langage de programmation Java, donc facilement portable sur différents ordinateurs. Il permet de cartographier rapidement des réseaux.

2/ Tout d'abord, ce serait bien que vous regardiez la vidéo de présentation du logiciel : http://www.vosviewer.com/getting-started. Puis d'avoir une idée de ce à quoi ressemble le logiciel : télécharger la version dédiée à la carte des champs scientifiques : http://www.vosviewer.com/features/examples#Scientific fields . Lancez le logiciel. Comment est obtenu cette "carte" ? A votre avis, le domaine que nous étudions se situera où dans cette carte de la science ?

3/ Maintenant que vous avez une idée de ce qu'est le logiciel, nous allons l'appliquer à un petit corpus pour prendre en main les options. Télécharger sur SCOPUS (export) en format CSV (fichier séparé par des virgules) l'ensemble des données des articles citant CRISPR Heroes (25). Ouvrir VOSviewer, créer une nouvelle carte basée sur des données bibliométriques, sélectionner ce fichier CSV (bien cliquer sur l'onglet SCOPUS) et puis choisir un type de réseau. Le mieux est que vous en fassiez plusieurs pour comprendre ce à quoi cela correspond:

- Un réseau de citation (qui cite qui) avec une unité de base qui est le document (l'article)
- Un réseau de co-occurence sur les mots-clés
- Une réseau de couplage bibliographique sur les documents

Essayez de comprendre comment chacun de ces réseau est construit (ce qu'il veut dire), et posez moi des questions si vous ne comprennez pas. A partir des réseaux, vous pouvez situer la publication CIRSPR Heroes dans le paysage des publications qui en font mention. Cela permet de poser de nouvelles questions (doit-on prendre en compte d'autres publications ? Quels traitements pourrait-on faire des mêmes données ?) et d'avoir une perspective plus générale sur les articles.

D'autres logiciels existent pour faire de l'analyse de corpus. Par exemple, Sci2Sci Tools, ou des plateformes en ligne comme Cortext. L'idée est cependant souvent la même : simplifier le traitement pour avancer plus vite dans la problématisation

## Passer à un corpus plus général

Analyser une publication c'est bien. Mais on aimerait maintenant s'intéresser à *$TOUTES** les publications sur CRIPSR. Faisons-le. 

4/ Sur Scopus, faites une requête qui permet de sélectionner tous les articles sur CRISPR. Faites quelques statistiques en utilisant directement l'onglet "analyse" de SCOPUS. Quel est l'article le plus cité ? Combien de publications en 2011 et combien en 2016 ? Quel taux de croissance ? Maintenant il faut télécharger ce corpus. Malheureusement, on ne peut télécharger que par tranche de 2000 : trouvez une astuce pour télécharger par bloc (par exemple, en filtrant par année). Puis réunissez tous les fichiers dans un même fichier.

5/ Utiliser VosViewer pour construire des cartes sur ce corpus de données. L'idée est de produire des visualisations qui permettent de poser de nouvelles questions. Ca signifie de tester, de regarder ce que ça donne, de se poser des questions, etc. Pour commencer :
- construire le réseau des co-citations d'articles pour identifier les articles les plus cités
- constuire le réseau des thématiques en termes de mots-clés, et en termes d'analyse de texte des résumés d'articles, pour identifier les domaines thématiques sur CRISPR


6/ A partir de ces premières visualisations exploratoires, quelles questions vous auriez envie de poser ? Quelles sont les limites rencontrées ? Par exemple, êtes-vous en mesure de poser la question de l'évolution des disciplines qui se sont intéressées à CRIPSR ? Ou d'identifier les technologies alternatives à CRISPR ? Ou d'identifier les articles qui parlent des risques ? Qu'est-ce qu'il faudrait pour faire ça à votre avis ? 

## Compléments facultatifs


