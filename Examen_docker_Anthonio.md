# INSTALLATION DE DOCKER 

Installation sur Linux (Ubuntu / Debian)

# 1. Mettre à jour le système

sudo apt update && sudo apt upgrade -y
"Cette commande est utilisée sous Linux (comme Ubuntu ou Debian) pour mettre à jour le système."

# 2. Installer les paquets nécessaires

sudo apt install apt-transport-https ca-certificates curl software-properties-common -y
"Elle sert à installer les outils nécessaires pour que ton système puisse télécharger et ajouter Docker de manière sécurisée."

# 3. Ajouter la clé GPG de Docker

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
"Elle télécharge et installe la clé GPG officielle de Docker, nécessaire pour que ton système fasse confiance aux paquets Docker."
"Ajouter la clé GPG officielle de Docker sur ton système pour que les paquets Docker puissent être vérifiés et authentifiés avant l’installation."

# 4. Ajouter le dépôt Docker

echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] \
https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | \
sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
"Cette commande permet d’ajouter le dépôt officiel de Docker à ton système Ubuntu."

# 5. Installer Docker

sudo apt update
sudo apt install docker-ce docker-ce-cli containerd.io -y
"Cette commande met à jour la liste des paquets disponibles sur ton système.
Comme tu viens d’ajouter le dépôt officiel de Docker, cette commande permet à apt de connaître les nouveaux paquets Docker disponibles."

# 6. Vérifier l’installation

docker --version
"sert à afficher la version installée de Docker sur ton système."







