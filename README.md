# README POUR THE HACKING BLOGGING

Deux gems supplémentaires ont été installé : gem table_print et la gem faker

## Projet de Lutz Jonathan, Wenger Marylis et Maxime Smolis


### Présentation du projet :

C'est un super blog où les utilisateurs pourront s'enregistrer, créer des articles, les commenter (sans pouvoir commenter les commentaires), attribuer une catégorie à chaque article et même les liker.


#### Consignes :

Un article a forcément un auteur (qui est un user) et un user peut avoir écrit plusieurs articles.
Un article a une catégorie, et une catégorie peut concerner plusieurs articles
Un utilisateur peut créer plusieurs commentaires, et un article peut avoir plusieurs commentaires.
Un utilisateur peut avoir plusieurs likes, et un article peut avoir plusieurs likes.


#### Résolution :

On a comme relation entre les tables:

User - 1,N - Article
Article - N,N - Categorie
User - 1,N - Like
Article - 1,N - Like


On a donc crée une base de donnée avec cinq tables et leurs attributs : 

- User : first_name, last_name, email
- Article : title, content, user_id (FK), category_id (FK)
- Categorie : name
- Comment : content
- Like : user_id (FK), article_id (FK)




### Fonctionnement du projet :

Dans un fichier seeds.rb, on a généré automatiquement des éléments à l'aide d'une boucle `times do` pour chaques tables grâce à la gem faker. Pour voir le resultat, se rendre dans `rails c` et utiliser la commande `tp NomTable.all`. Enjoy ;) 
