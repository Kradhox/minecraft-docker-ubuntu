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
   git clone https://github.com/Kradhox/minecraft-docker-ubuntu
   cd minecraft-docker-ubuntu/src
   ```

### Étape 3 : Récupération du modpack serveur

1. **Télécharger le modpack** :

   https://www.curseforge.com/minecraft/modpacks/roguelike-adventures-and-dungeons-2/files/4777217

2. **Déposer le zip du modpack sur le serveur**

   Créer un répertoire "downloads" dans le dossier du `docker-compose.yml`
   ```bash
   mkdir downloads
   ```

   Se connecter au serveur avec FileZilla en SFTP pour déposer le fichier dans le répertoire

