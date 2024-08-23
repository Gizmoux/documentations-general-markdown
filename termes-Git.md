# git init

Initialise un nouveau dépôt Git dans le répertoire courant.

# git clone

Crée une copie locale d'un dépôt distant.

# git add

Ajoute des fichiers à l'index (staging area) en préparation d'un commit.

# git commit

Enregistre les modifications dans l'historique du dépôt avec un message descriptif.

# git status

Affiche l'état actuel du dépôt, montrant les fichiers modifiés, ajoutés ou supprimés.
g# it push
Envoie les commits locaux vers un dépôt distant.

# git pull

Récupère et fusionne les modifications d'un dépôt distant dans votre branche locale.

# git branch

Liste, crée ou supprime des branches.

# git checkout

Bascule entre différentes branches ou restaure des fichiers de travail.

# git merge

Fusionne une branche dans la branche active

# git fetch

Récupère les dernières modifications d'un dépôt distant sans les fusionner dans votre branche locale.

# git diff

Affiche les différences entre les fichiers du répertoire de travail et ceux de l'index ou entre l'index et le dernier commit.

# git stash

Enregistre temporairement les modifications non commitées pour pouvoir basculer sur une autre branche.

# git log

Affiche l'historique des commits du dépôt.

# git reset

Permet de réinitialiser l'état du dépôt à un commit spécifique, avec différentes options pour gérer les modifications

### Git Reset

Cette commande est utilisée pour annuler des changements ou déplacer la branche HEAD vers un commit spécifique. Elle a trois modes principaux :
--soft : Déplace uniquement HEAD vers le commit spécifié, laissant les modifications dans l'index.
--mixed (par défaut) : Déplace HEAD et met à jour l'index, mais laisse les fichiers du répertoire de travail intacts.
--hard : Déplace HEAD, met à jour l'index et le répertoire de travail pour correspondre au commit spécifié.
Attention : L'option --hard peut entraîner une perte de données si utilisée sans précaution, car elle écrase les fichiers du répertoire de travail.
git reset peut également être utilisé avec un chemin de fichier pour désindexer des fichiers spécifiques sans modifier HEAD.
Ces commandes supplémentaires, en particulier git reset, offrent un contrôle plus fin sur la gestion de l'historique et de l'état de votre dépôt Git.

# Git rebase

Git rebase est une opération qui consiste à prendre une branche et à la "transplanter" sur une autre base, généralement la pointe d'une autre branche. Concrètement, cette commande :
Copie les commits de la branche source
Les réapplique un par un sur la nouvelle base
Le résultat est un historique linéaire et plus propre, sans commits de fusion superflus
