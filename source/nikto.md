# Cours

## Qu’est ce que Nikto ?
Nikto est une application open source créée en 2001 qui permet de scanner des serveurs web. Il permettra de donner des informations sur de potentielle vulnérabilités par exemple.

## Que peut-il nous donner comme informations ?
Nikto est capable de :
* trouver des injections SQL,XSS et autres types de vulnérabilité. 
* Deviner des sous-domaines
* Sauvegarder des rapport dans des fichier HTML,CSV ou XML
* Identifier les logiciels installés
* Exporter vers Metasploit
* Deviner des identifiants/mot de passe faciles à trouver

## Comment télécharger Nikto ?
Comme beaucoup d’outils de pentesting, Nikto est présent par défaut sur Kali Linux.
Si vous avez une autre distribution Linux (debian) vous pourrez l’installer par la commande ```apt-get install nikto```. Sinon, vous pouvez vous rendre sur Github : https://github.com/sullo/nikto

## Comment utiliser Nikto ?
Pour voir toutes les possibilités et commandes de nikto, la première commande à taper est :

```nikto -Help```.

Vous verrez tout un tas d’options expliquées par la suite. La plus simple et la plus utilisée sera la commande : 
```nikto -h <target>``` en remplaçant la target par une adresse ip ou un nom de domaine.

D’autres options complémentaires pourront s’ajouter à cette commande telles que : ```-id``` qui servira à renseigner une combinaison ```identifiant:motdepasse``` pour se connecter sur la cible, ou encore   ```-mutate``` pour découvrir de nouveaux fichiers ou dossiers cachés.

Si l’on veut scanner un domaine en https, il faudra ajouter le tag ```-ssl``` pour scanner le port 443.

Il est aussi possible de scanner plusieurs adresses IP en même temps. Par exemple en les mettant dans un fichier texte et en tapant la commande : ```nikto -h adresses.txt```

# Challenge

## Objectif du challenge : 
trouver le numéro OSVDB de la potentielle vulnérabilité de la machine docker déployée.

## Que faut-il faire ?
Récupérer les machines : 

* Télécharger le fichier [docker-compose.yml](./nikto//docker-compose.yml)

* Déployer et utiliser les machines : 

```console 
docker-compose up -d
docker exec -it nikto_machine /bin/bash
```

* Analyser la machine avec nikto et lire le numéro OSVDB de la vulnérabilité trouvée.