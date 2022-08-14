Docker
=======

Introduction : Pourquoi utiliser Docker
----------------------------------------

Nous utilisons ici la technologie Docker car cette dernière vous permettra d'avoir des machines conçues exprès pour vous entrainer aux techniques de hacking/pentest.
Grâce à cela, vous pourrez télécharger des machines avec les logiciels directement installés pour vous pour chaque session, ce qui vous évite de perdre du temps à l'installation lorsque vous lisez un tutoriel sur notre site. En effet, lorsqu'on lit un tutoriel n'importe où sur le web, la première chose que nous voulons faire est de tester sois-même. Nous sommes souvent frustrés par le temps que met l'installation, par les problèmes de compatibilité des machines, on a jamais la même machine que la personne qui propose le turoriel, etc. 
Docker nous évite tous ces problèmes puisque tout le monde téléchargera la même machine (image) et le tutoriel que nous proposerons sera lui aussi effectué sur ces mêmes machines.


Installation
------------

Vite ! Maintenant que vous savez pourquoi il vous faut Docker, passons à l'installation !
C'est le seul moment sur ce site où vous pourrez rencontrer des problèmes de compatibilité... Mais nous allons essayer de vous donner le plus de détails possible pour vous aider !

Sur quelle machine vous êtes ?
--------------------------------

Plusieurs réponses possible ici : Mac, Windows ou Linux.
Si vous êtes sur une machine Linux, il vous faut savoir quelle distribution vous avez (exemple : Debian/Fedora/Ubuntu/Arch).

Installation en fonction du système
-------------------------------------

Nous allons vous rediriger sur les bons liens de la documentation d'installation Docker puisqu'elle est très claire lorsqu'on lit au bon endroit. Il nous paraissait inutile de vous réécrire les mêmes étapes d'installation ici.

Installation sur Mac
^^^^^^^^^^^^^^^^^^^^

Rendez vous ici : https://docs.docker.com/desktop/install/mac-install/

Vous devrez au cours de l'installation savoir si vous avez une version Intel ou Apple Silicon (gammes M1/M2)

Installation sur Windows
^^^^^^^^^^^^^^^^^^^^^^^^^

Rendez-vous ici : https://docs.docker.com/desktop/install/windows-install/

Installation sur Linux
^^^^^^^^^^^^^^^^^^^^^^^

Rendez-vous ici : https://docs.docker.com/desktop/install/linux-install/

Vérifier son installation
--------------------------

Pour vérifier que l'installation est faite, veillez ouvrir un Terminal/invite de commandes et taper la commande "docker". Si vous avez une réponse du type ```Usage:  docker [OPTIONS] COMMAND``` tout est bon. Sinon il vous faut revoir l'installation.

Installation de docker-compose
-------------------------------

Pour faire fonctionner plusieurs machines ensemble, les faire communiquer entre elles, créer des réseaux, etc. Nous utilisons la technologie docker-compose qu'il vous faudra aussi installer pour que tout se passe bien sur le site :)

Si pendant votre installation vous avez aussi installé l'application Docker Desktop, bien joué, vous devriez déjà avoir docker-compose !! (Sous Mac et Windows, vous devriez l'avoir installée).

Si vous êtes sous Linux et que vous n'avez pas installé Docker Desktop, je vous propose d'aller ici : https://docs.docker.com/compose/install/compose-plugin/#installing-compose-on-linux-systems