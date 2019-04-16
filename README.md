# Mcommerce-partie1
Activité du tuto "Construisez des Microservices" de OpenClassRooms

# Consignes pour la réalisation
A la fin de chaque partie, créez un commit  et poussez le vers votre projet GitHub

# Partie 1 - Affichage de la marge
La méthode calculerMargeProduit doit répondre à  une requête GET sur l’URI   /AdminProduits. Les données doivent être récupérées depuis la base de données mises en place dans le projet.

Voici un exemple de réponse attendue : 

{
"Product{id=1, nom='Ordinateur portable', prix=350}": 230,
"Product{id=2, nom='Aspirateur Robot', prix=500}": 300,
"Product{id=3, nom='Table de Ping Pong', prix=750}": 350
}
 
# Partie 2 - Tri par ordre alphabétique
La méthode  trierProduitsParOrdreAlphabetique doit impérativement faire appel à une méthode que vous allez ajouter dans ProductDao  qui utilise le nommage conventionné de Spring Data JPA pour générer automatiquement les requêtes. Voici le résultat à obtenir avec le contenu de la base de données du cours :

{
{
"id": 2,
"nom": "Aspirateur Robot",
"prix": 500,
"prixAchat": 200
},
{
"id": 1,
"nom": "Ordinateur portable",
"prix": 350,
"prixAchat": 120
},
{
"id": 3,
"nom": "Table de Ping Pong",
"prix": 750,
"prixAchat": 400
}
}

# Partie 3 - Validation du prix de vente
Si le prix de vente est de 0, lancez une exception du nom de  ProduitGratuitException  (à créer) qui retournera le bon code HTTP pour ce cas avec un message explicatif que vous définirez.

# Partie 4 - Test des méthodes créées
Suivez les étapes suivantes pour écrire la collection, l'exécuter et founir le résultat pour votre testeur :

Créez un dossier  TestsPostman à la racine de votre projet
Dans Postman, créez une collection pour définir vos tests
Faites une capture d'écran du résultat de l'exécution de la collection
Exportez la collection au format JSON  dans le dossier  TestsPostman
Commitez et poussez vers le dépôt GitHub
