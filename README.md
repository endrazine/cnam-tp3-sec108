
# CNAM TP3 : Installation d'un serveur sécurisé Ubuntu SERVER 20.04 LTS

Le but de ces Travaux Pratiques est d'installer un serveur web sous Ubuntu 20.04 LTS version server.

## Resultats

Ces TPs sont notés : prière de m'envoyer vos résultats (captures d'écrans, liste des commandes utilisés, sortie de la commande "mount", fichiers /etc/ssh/sshd_config et fichiers de configuration nginx) sous 1 semaine, sur mon email du CNAM.

## Installation d'un serveur Ubuntu 20.04 LTS version serveur

Télécharger l'iso de la version d'Ubuntu 20.04 LTS depuis le site officiel d'Ubuntu:

	jonathan@blackbox:~/CNAM/tp3$ wget https://releases.ubuntu.com/20.04.3/ubuntu-20.04.3-live-server-amd64.iso                                                         
	--2021-09-17 13:13:45--  https://releases.ubuntu.com/20.04.3/ubuntu-20.04.3-live-server-amd64.iso
	Resolving releases.ubuntu.com (releases.ubuntu.com)... 2001:67c:1562::25, 2001:67c:1562::28, 91.189.91.124, ...
	Connecting to releases.ubuntu.com (releases.ubuntu.com)|2001:67c:1562::25|:443... connected.
	HTTP request sent, awaiting response... 200 OK
	Length: 1261371392 (1.2G) [application/x-iso9660-image]
	Saving to: 'ubuntu-20.04.3-live-server-amd64.iso'

	ubuntu-20.04.3-live-server-amd64.iso                 100%[=====================================================================================================================>]   1.17G  3.34MB/s    in 5m 1s   

	2021-09-17 13:18:47 (4.00 MB/s) - 'ubuntu-20.04.3-live-server-amd64.iso' saved [1261371392/1261371392]

	jonathan@blackbox:~/CNAM/tp3$

Suivre le tutorial suivant permettant de chiffrer la partition /home avec LUKS: https://doc.ubuntu-fr.org/tutoriel/chiffrer_son_disque

### Partitionning

Créer une partition /tmp séparée.

Créer une partition /var séparée.

Créer une partition /home séparée

Chiffrer la partition /home avec LUKS

### Installation/Hardening

Suivre le guide d'installation Debian vu en cours, l'adapter aux besoins d'un serveur Ubuntu.

### Installer les mises à jour de sécurité automatiques

Confère https://help.ubuntu.com/community/AutomaticSecurityUpdates

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


### Cracking de passwords avec John the ripper

Céer un utilisateur avec un mot de passe faible.

Utiliser la commande "john" pour tenter de casser ce password faible.

### Résultats

Envoyer vos résultats sur mon email du CNAM : jonathan.brossard at lecnam.net


### J'ai fini plus tôt !

Good for you ! S'attacher à réaliser les wargames disponibles ici pour progresser: https://overthewire.org/wargames/



