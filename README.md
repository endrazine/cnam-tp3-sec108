
# CNAM TP1 : Installation d'un serveur sécurisé Ubuntu SERVER 20.04 LTS

Le but de ces Travaux Pratiques est d'installer un serveur web sous Ubuntu 20.04 LTS version server.

## Resultats

Ces TPs sont notés : prière de m'envoyer vos résultats (captures d'écrans, liste des commandes utilisés, sortie de la commande "mount", fichiers /etc/ssh/sshd_config et fichiers de configuration nginx) sous 1 semaine, sur mon email du CNAM.

## Installation d'un serveur Ubuntu 20.04 LTS version serveur

Télécharger l'iso de la version d'Ubuntu 20.04 LTS depuis le site officiel d'Ubuntu.

### Partitionning

Créer une partition /tmp séparée.

Créer une partition /home séparée

Chiffrer la partition /home avec LUKS

### Installation/Hardening

Suivre le guide d'installation Debian vu en cours, l'adapter aux besoins d'un serveur Ubuntu.

### Modification du umask

Modifier le umask pour tout le systeme.

Créer un nouvel utilisateur : cnam. Que pensez vous des permissions sur /home/cnam ?

### Acces à distance via ssh par clé

Installer openssh-server.

Vérifiez que vous pouvez vous connecter au compte cnam via ssh.

Générer une paire de clés publiques/privés RSA 2048 au moyen de la commande ssh-keygen.

Copier la clé publique dans /home/cnam/.ssh/authorized_keys

Modifier le fichier /etc/ssh/sshd_config pour ne permettre l'authentification que via des clés ssh.


### Installation d'un serveur Nginx

Installer un serveur nginx.

Modifier la configuration de nginx en editant les fichiers sous /etc/nginx/ afin de n'authoriser que les connections https.

Générer des certificats autosignés et les installer pour nginx.


### Résultats

Envoyer vos résultats sur mon email du CNAM : jonathan.brossard at lecnam.net


### J'ai fini plus tôt !

Good for you ! S'attacher à réaliser les wargames disponibles ici pour progresser: https://overthewire.org/wargames/



