## Bases de Données : MongoDB, MySQL et PostgreSQL

### Concepts Généraux

- **SGBD** : Système de Gestion de Base de Données
- **ACID** : Atomicité, Cohérence, Isolation, Durabilité (propriétés des transactions)
- **Transaction** : Séquence d'opérations traitée comme une unité indivisible
- **Index** : Structure de données pour améliorer la vitesse de récupération des données
- **Clé primaire** : Identifiant unique pour chaque enregistrement dans une table
- **Clé étrangère** : Champ qui fait référence à la clé primaire d'une autre table

### MongoDB (NoSQL)

- **Document** : Unité de base de stockage dans MongoDB (similaire à une ligne dans SQL)
- **Collection** : Groupe de documents (similaire à une table dans SQL)
- **BSON** : Format binaire utilisé par MongoDB pour stocker les documents
- **id** : Identifiant unique automatiquement généré pour chaque document
- **Agrégation** : Framework pour effectuer des opérations de traitement de données
- **Replica Set** : Groupe de serveurs MongoDB maintenant les mêmes données
- **Sharding** : Méthode de distribution des données sur plusieurs serveurs

### MySQL et PostgreSQL (SQL)

- **Table** : Structure qui organise les données en lignes et colonnes
- **Ligne/Tuple** : Un enregistrement unique dans une table
- **Colonne/Attribut** : Définit le type de données stockées
- **SQL** : Structured Query Language, langage utilisé pour interagir avec la base de données
- **JOIN** : Opération pour combiner des lignes de deux ou plusieurs tables
- **View** : Table virtuelle basée sur le résultat d'une requête SQL
- **Stored Procedure** : Ensemble de requêtes SQL stockées et réutilisables

### Spécifique à MySQL

- **InnoDB** : Moteur de stockage par défaut de MySQL
- **MyISAM** : Ancien moteur de stockage de MySQL
- **Event Scheduler** : Fonctionnalité pour planifier et exécuter des tâches

### Spécifique à PostgreSQL

- **MVCC** : Multi-Version Concurrency Control, gestion de la concurrence
- **Hstore** : Type de données pour stocker des paires clé-valeur
- **PL/pgSQL** : Langage procédural pour PostgreSQL
- **Inheritance** : Capacité d'une table à hériter des caractéristiques d'une autre table

### Indexation

- **B-tree** : Structure d'index par défaut dans la plupart des SGBD
- **Hash** : Type d'index utilisé pour les recherches d'égalité exacte
- **GiST** : Generalized Search Tree, utilisé pour les données géospatiales dans PostgreSQL

### Optimisation

- **Query Plan** : Plan d'exécution d'une requête
- **EXPLAIN** : Commande pour afficher le plan d'exécution d'une requête
- **Partitionnement** : Division d'une grande table en plusieurs parties plus petites

### Sauvegarde et Récupération

- **Dump** : Copie de la base de données sous forme de fichier
- **Point-in-Time Recovery** : Capacité de restaurer la base de données à un moment précis
- **WAL** : Write-Ahead Logging, méthode pour assurer l'intégrité des données

### Réplication et Haute Disponibilité

- **Master-Slave Replication** : Configuration où les données sont copiées du serveur maître vers un ou plusieurs serveurs esclaves
- **Clustering** : Regroupement de plusieurs serveurs pour améliorer la disponibilité et les performances
