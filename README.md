# Reseaux2







Quels sont les protocoles qui ont été remplacés par SSH ?

-RLOGIN

-TELNET

-RSH

-FTP


Quelles sont les différents modes d'utilisation de SSH (notamment au niveau de la sécurité) ?

Acces a distance a la console.

Transférer des fichier via la console.

-SCP (Secure Copy)

-SFTP (SSH File Transfert Protocol)

-SSHFS (SSH File System)

-X11 Forwarding

Comment est établie une connection SSH entre un client et un serveur avec la méthode la plus sécurisé ?

![ssh_handshake.svg](..%2F..%2FT%C3%A9l%C3%A9chargements%2Fssh_handshake.svg)








Liste commande terminal Linux : 

-CD = "Change Directory" Passer au repertoire auquel vous essayez d'accéder.



-PWD = "Print Working Directory" affiche le chemin absolu du repertoire dans le quel on se trouve.



-MV = Déplacer ou renommer des fichiers et des repertoires dans votre système de fichiers.



-MKDIR = Créer un repertoire dans le shell, en spécifiant le nom du nouveau répertoire.



-Touch = Mettre a jour les temps d'accès et de modifications des fichiers spécifiés.



-Less = Inspecter un fichier en avant et en arrière.




-Grep = Recherche les lignes qui correspondent a une éxpression régulière et les affiches.




-Find = Recherche des fichiers dans une hiérarchie de répertoires en se basant sur une expression regex.




-Rsync = "remote synchro" Mettre en place des systeme de sauvegarde distante ou des points de restauration du système.





-Nano = Ouvrir une fenetre d'édition (en créant ou ouvrant une fentre d'édition.)

------


Itération 2 : 

PHP-FPM = (FastCGI Process Manager) est une interface SAPI permettant la communication entre un serveur Web et PHP, basée sur le protocole FastCGI

PHP-FPM créé en 2004 par Andrei Nigmatulin constitue une alternative au serveur PHP avec des options pour les sites subissant de fortes charges.

Contrairement au serveur PHP, il est fourni avec son propre daemon.



NGINX = Est un logiciel libre de serveur Web(ou HTTP) ainsi qu'un proxy inverse écrit par Igor Sysoev, dont le développement a débuté en 2002 pour les besoins d'un site russe a très fort trafic(Rambler).

La documentation est disponible dans plusieurs langues, c'est depuis avril 2019, le serveur web le plus tuilisé du monde après Netcraft, ou le deuxième serveur le plus utilisé d'après W3tchers.

Outre le fait d'être un serveur HTTP, NGINX peut être configuré pour être un serveur mandataire inverse (en anglais : reverse proxy) Web et un serveur proxy de messagerie électronique (IMAP / POP3). L'utilisation la plus fréquente de NGINX est de le configurer comme un serveur Web classique pour servir des fichiers statiques et comme un proxy pour les requêtes dynamiques typiquement acheminées en utilisant une interface FastCGI vers un ou des serveurs applicatifs avec un mécanisme de répartition de charge.



Intéraction entre PHP-FPM, NGINX, et notre code = 





![téléchargement (2).jpeg](..%2F..%2FT%C3%A9l%C3%A9chargements%2Ft%C3%A9l%C3%A9chargement%20%282%29.jpeg)
  



![téléchargement.png](..%2F..%2FT%C3%A9l%C3%A9chargements%2Ft%C3%A9l%C3%A9chargement.png)


Problématique = Se retrouver rapidement avec des compatibilité et problémes de légereté, des languages ou versions différentes feront vite apparaitre des problèmes, et vous devrez faire appel a des VM, et cela risque de devenir très lourd.



-----

1 — La conteneurisation et Docker : c’est quoi ?


L'informatique, à l'instar de nombreux domaines technologiques, est caractérisée par
une évolution constante et rapide. Au fil du temps, des outils et des méthodes ont été
développés pour répondre à des problèmes spécifiques. Docker, avec sa proposition
innovante de conteneurisation, est l'un de ces outils qui a radicalement transformé la
manière dont nous développons, déployons et exécutons les logiciels.



L'évolution du déploiement et de la mise en production :



1. Déploiement manuel sur serveur physique :
   Avant l'automatisation, tout était manuel. Les administrateurs système devaient
   installer chaque composant individuellement, ce qui posait d'énormes problèmes de
   cohérence et de reproductibilité.

   

2. Machines virtuelles (VM) :
   La virtualisation a permis d'isoler les applications, mais chaque VM était lourde, avec
   son propre système d'exploitation, et prenait du temps à démarrer et à arrêter.
   Ces méthodes traditionnelles ont jeté les bases pour comprendre les défis que Docker
   visait à résoudre.

----

Docker et la naissance de la conteneurisation moderne :

Docker a été introduit en 2013 par Solomon Hykes. Si la technologie de
conteneurisation n'était pas nouvelle, Docker l'a rendue pratique, efficace et populaire.
Les conteneurs offrent :


● Isolation

● Portabilité

● Efficacité

● Scalabilité

En somme, Docker et la conteneurisation ont été la réponse à une série de défis
persistants dans le monde de l'informatique. En combinant la reproductibilité, la
portabilité et l'efficacité, ils ont offert une solution élégante aux problèmes que les
méthodes traditionnelles peinaient à résoudre. La popularité croissante de Docker
témoigne de son impact profond et de son rôle central dans le paysage technologique
moderne.



Les avantages de la conteneurisation et ses grands principes : 



Flexible : Toute application peut être transformé en conteneur.


Léger : Contrairement a la virtualisation classique, Docker exploite et partage le kernel du système d'éxploitation de l'hôte, ce qui le rends très éfficace en terme d'utilisation des ressources du système.


Portable : Il est possible de créer déployer et démarrer des conteneurs sur son ordinateur, celui de ses clients ou un serveur distant.


Auto-suffisant : L'installation et la désinstallation de conteneurs ne dépend pas des autres conteneurs installés. 

Ce qui permet de mettre à jour ou remplacer un conteneur sans modifier les autres.


Scalable : Dupliquer un container est éxtremement simple, ce qui permet de réaliser de la scalabilité horizontale aisément.


Sécurisé : Par défaut, Docker crée des conteneurs en appliquant des règles de sécurité strictes et isole les processus.


4. Pour qui Docker est bénéfique ?


   Pour les développeurs :

   En utilisant Docker les développeurs sont donc sûrs que leur application fonctionnera indépendamment du système d’exploitation et de l’environnement auquel il sont soumis.

Ainsi ils peuvent se concentrer sur la production de code plutôt que de passer du temps à penser au système sur lequel l’application fonctionnera.

Pour les administrateurs systèmes :

Docker permet d’installer et de démarrer des conteneurs qui fonctionnent ensembles.

Combiné avec docker-compose il est possible de déployer toute une application et ses dépendances avec une seule commande.

Enfin les installations de mises à jours peuvent être simplifiées par une configuration facile à implémenter.


2 — Docker : les concepts de base

Docker repose sur plusieurs concepts clés qui permettent de comprendre son
fonctionnement et son utilité. Voici les concepts de base associés à Docker :

● Image : Une image Docker est un modèle immuable utilisé pour créer un
conteneur. Elle contient le code source de l'application, les bibliothèques, les
dépendances et autres fichiers nécessaires à l'exécution de l'application.

● Dockerfile : C'est un fichier de script qui contient les instructions pour
construire une image Docker.

● Conteneur : Un conteneur est une instance exécutable d'une image Docker. Il
s'agit d'une encapsulation légère d'une application et de son environnement
d'exécution, fonctionnant de manière isolée sur le système hôte.

● Registry : Zone de stockage pour les images Docker. Il peut être public ou privé
(pour une utilisation interne en entreprise par exemple). Docker Hub est un
service cloud public pour partager et stocker des images Docker. C'est comme
un "GitHub" pour les images Docker, où les développeurs peuvent push ou pull
des images.

● Volume : Les volumes sont utilisés pour persister les données et partager des
fichiers entre le conteneur et l'hôte. Ils sont essentiels pour éviter la perte de
données lorsque les conteneurs sont arrêtés ou supprimés.

● Réseau Docker : Docker possède sa propre gestion du réseau, permettant aux
conteneurs de communiquer entre eux et avec des ressources extérieures. Il
offre plusieurs modes réseau comme "bridge","host" et"overlay"

● Docker Compose : C'est un outil pour définir et gérer des applications
multi-conteneurs. Avec Docker Compose, on peut définir une application à
l'aide de plusieurs conteneurs dans un seul fichier, puis démarrer ces conteneurs
simultanément avec une seule commande. Par exemple, vous voulez déployer
une application PHP qui utilise une base de données MySQL. Vous allez écrire
un fichier docker-compose qui va décrire la configuration du conteneur pour
PHP et le conteneur MySQL. Cela va éviter de lancer les commandes à la main
et permettre d’avoir un suivi dans Git.
 -----




Non mes données ne sont plus présente.




Statefull & Stateless =

Statefull =



Une application avec état, en revanche, peut se souvenir d'au moins quelques éléments de son état à chaque fois qu'elle s'exécute. Les données d'état réelles qu'elle stocke peuvent dépendre de l'application et des conditions dans lesquelles elle fonctionne. La plupart des applications que nous rencontrons au quotidien ont au moins un certain niveau d'état. Elles stockent nos préférences, gardent une trace de la taille et de l'emplacement de la fenêtre et se souviennent des fichiers qu'elles ont ouverts récemment.





Stateless = 

Une application sans état est une application qui ne lit ni ne stocke d'informations sur son état d'une fois à l'autre.

Dans ce cas, le terme "état" peut désigner toute condition modifiable, y compris les résultats des opérations internes, les interactions avec d'autres applications ou services, les préférences définies par l'utilisateur, les variables d'environnement, le contenu de la mémoire ou du stockage temporaire, ou encore les fichiers ouverts, lus ou écrits. Si l'application de calculatrice de votre téléphone démarre toujours avec zéro à l'écran, rien dans les registres et aucun historique des calculs passés, elle est sans état.

VolumeDocker = 



Un volume Docker fournit un mécanisme pour assurer la persistance des données d'un conteneur ou lui permettre « d'échanger » des données avec d'autres conteneurs partageant le même volume. Un volume Docker est initialisé lors de la création d'un conteneur et est monté dans le conteneur comme un système de fichiers.





Le volume docker permet au conteneur au relancement d'aller chercher ce fichier volume en question puis de faire le lien directement afin de récupérer les données précédement enregistré dans la base de données.

Principes de docker : 



Portabilité : Recrée ou relancer rapidement un conteneur facilement, partager la configuration a un autre environement facilement ce qui permet d'avoir la meme config partout.


Efficacité : Les applis conteneurisé utilisent beaucoup moins de ressources que des machines virtuelles car elles utilisent le même noyau(*), l'arrêt et le démarrage sont également bien plus rapide.
Copié un conteneur peut également permettre d'en augmenter les requetes, exemples : j'ai un conteneur qui contient un site qui peut supporter un total de 1000 requetes, je copie le conteneur avec le meme contenant et j'ai un site qui peut recevoir 2000 requetes. (en gros)


Isolation = Pouvoir utilisé sur des serveurs très inférieur ou très supérieur en les "copiant", permettre également de combiner plusieurs languages différent dans des conteneurs différents sans causer de vrais problème ou de casse dans les codes ou la réalisation de certaine manipulation.
Dépendances ou configuration n'affecteront aucunes dépendances ou configuration d'une ou plusieurs autres conteneurs.


Scalabilité : Crée des copies d'un conteneurs afin d'augmenter les requetes maximal recu, déployé et supprimer rapidement les conteneurs, 




 