# Initial setup

Une fois Unbuntu Server d'installé.
Commençons par la première étape qui sera l'installation de Docker et Docker Compose sur votre serveur Ubuntu. 

### Étape 1 : Installation de Docker et Docker Compose

1. **Mise à jour des paquets** :
   Avant d'installer Docker, il est prudent de mettre à jour la liste des paquets disponibles pour s'assurer que nous obtenons la version la plus récente.

   ```bash
   sudo apt update
   ```

2. **Installation de Docker** :
   Nous utiliserons le gestionnaire de paquets APT pour installer Docker.

   ```bash
   sudo apt install docker.io
   ```

   Cette commande installera Docker et toutes les dépendances nécessaires. Docker permettra de créer et gérer des conteneurs pour votre serveur Minecraft.

3. **Démarrage de Docker** :
   Activez Docker pour qu'il démarre au démarrage, et démarrez le service Docker.

   ```bash
   sudo systemctl enable docker
   sudo systemctl start docker
   ```

4. **Installation de Docker Compose** :
   Docker Compose est un outil qui aide à définir et gérer des applications multi-conteneurs avec Docker. Il sera utile pour gérer votre serveur Minecraft et d'autres services associés.

   ```bash
   sudo apt install docker-compose
   ```

5. **Vérification des installations** :
   Vérifiez que Docker et Docker Compose sont installés correctement.

   ```bash
   docker --version
   docker-compose --version
   ```

### Étape 2 : Récupération du Répertoire GitHub

1. **Installation de Git** :
   Si Git n'est pas déjà installé sur votre serveur, installez-le avec la commande suivante :

   ```bash
   sudo apt install git
   ```

2. **Clonage du Répertoire** :
   Clonez le répertoire GitHub contenant les fichiers de configuration et le Docker Compose sur votre serveur :

   ```bash
   git clone https://github.com/[Votre-Username]/minecraft-server.git
   cd minecraft-server
   ```

   Remplacez `[Votre-Username]` par votre nom d'utilisateur GitHub et `minecraft-server` par le nom de votre répertoire.

3. **Exploration des Fichiers** :
   Explorez les fichiers et dossiers clonés pour vous familiariser avec la structure du projet :

   ```bash
   ls
   ```

Cette étape permettra aux utilisateurs de récupérer tous les fichiers nécessaires pour configurer et lancer le serveur Minecraft moddé. Ils seront prêts à passer à l'étape de configuration dans la suite du tutoriel.

Faites-moi savoir si cette structure vous convient ou si des ajustements sont nécessaires avant de passer à l'étape suivante.