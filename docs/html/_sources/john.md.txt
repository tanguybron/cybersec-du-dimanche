# Cours

## A quoi sert John ?

L’outil John va nous être très utile pour le cracking de mot de passe. En effet, si un attaquant parvient d’une manière ou d’une autre à récupérer une base de donnée d’un site contenant les identifiants et mots de passe des utilisateurs, la grande majorité du temps, ce dernier ne pourra pas lire le mot de passe directement. En effet, une sécurité a été ajoutée pour stocker les mots de passe au cas où ce genre de situation arriverait.

Sans entrer dans les détails, les mots de passe sont stockés sous forme de hash, ce qui correspond à passer le mot de passe de l’utilisateur dans une fonction complexe à sens unique. Ce qui signifie que même avec un hash, il est impossible de récupérer directement le mot de passe en clair. Lors de la connexion le hash entré et le hash stocké sont comparés pour voir si ce sont les mêmes.

Cependant il n’est pas impossible de trouver un mot de passe à partir du hash.

John nous permet d’effectuer une attaque brute force simple, ou par dictionnaire lorsque nous avons un ou plusieurs hashes à disposition.

## Comment lancer l'attaque brute force avec John ?

Imaginons un fichier mdp.hashes contenant le hash d’une session. Le fichier pourrait contenir une ligne comme suit : 

```
jeremy:$1$XT.ZwPx4$LpAfbyGhDRZ3QSxdCzUqD/:19123:0:99999:7:::
```

où

```
$1$XT.ZwPx4$LpAfbyGhDRZ3QSxdCzUqD/
```

correspond au hash du mot de passe de connexion.

Ainsi john pourra nous être utile à casser le mot de passe par une attaque par dictionnaire en tapant la commande suivante :

```shell
john -w=liste.txt mdp.hashes
```

Ainsi cette ligne demande à john de calculer tous les hash des mots contenus dans liste.txt et de le comparer au hash de la session. Si les deux hashes sont les mêmes, alors le mot de passe est trouvé et John s’arrête.

## Entrainement et mise en situation réelle

Pour voir si vous avez bien compris le cours, je vous propose de vous entrainer sur un docker que j'ai créé spécialement pour cela.

### Que devez-vous faire ?

Il vous faut docker installé (il existe tout un tas de tutoriels qui vous expliquerons comment le télécharger)
quand docker et docker-compose sont installés sur votre machine, nous pouvons passer à la suite : 

Il vous faut télécharger le fichier [docker-compose.yml](./john-the-ripper/docker-compose.yml)

Ensuite, il vous restera quelques commandes à connaître : 


```shell
    docker-compose up -d
    docker exec -it martin /bin/bash
    docker exec -it john /bin/bash
```

La première commande vous permet de créer les deux machines dont vous aurez besoin. La machine de martin correspond à la machine victime et la machine john à celle de l'attaque qui possède l'outil john installé dessus.

### Objectifs

#### Situation
Martin veut mettre sa machine à jour avec ```apt-get update```, mais pour cela il doit être root sur sa machine. Malheureusement il ne connait pas son mot de passe administrateur car c'est son ami Jeremy qui a configuré sa machine ! Ce dernier ne se souvient plus du tout du mot de passe non plus :( Arriverez-vous à trouver le mot de passe administrateur de cette machine pour la mettre à jour ?

#### Que faire ?
* Récupérer les mots de passe hachés de session
* Cracker le hash avec John d'une session susceptible d'avoir les accès root
* Connectez vous avec la session dont vous avez trouvé le mot de passe
* Tapez la commande ```apt-get update```

Si la machine est à jour vous avez accompli votre mission. Félicitations

### Vidéo de résolution
[vidéo youtube](https://youtu.be/5X0gQ5gLaO0)