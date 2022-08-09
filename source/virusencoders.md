# Virus Encoders

## Msfvenom : est-il possible de tromper l'antivirus ?

msfvenom est un outil de création de payloads (charge utile en français).

Cet outil propose un grand nombre de personnalisations (encodage, chiffrement, taille maximale du fichier…,).
En créant un payload, l’objectif principal d’un attaquant sera de prendre le contrôle d’une machine victime à
distance, notamment à l’aide d’un reverse shell.
Cependant, bon nombre d'anti-virus arrivent désormais à détecter et à bloquer le fonctionnement de ce genre de
fichiers lorsqu’ils sont téléchargés.


Ainsi les pirates ont mis en place des techniques afin de rendre de moins en moins détectables ces fichiers.
Pour commencer, ils ont pensé à chiffrer le payload avec une clef de chiffrement
et créer un exécutable qui le déchiffre et l'exécuter ensuite sur la machine victime. Malheureusement, maintenant
les antivirus détectent tous les programmes chiffrés comme malveillants
(la signature du crypteur est détectée dans ce cas-là).


Une autre idée leur est venue, celle de l’encodage. Cela consiste, comme la technique de chiffrement, à mettre
le payload sous une autre forme pour qu’il soit moins détectable, mais
cette fois-ci sans utiliser de clef de chiffrement. L’encodeur le plus connu est shikata_ga_nai, il a une très
bonne réputation, mais il a été beaucoup trop utilisé, donc les antivirus
sont désormais capables de le détecter. En voyant que les antivirus détectent un fichier encodé, la possibilité
d’encoder plusieurs fois de suite un même fichier a été trouvée, c'est-à-dire
encoder avec un nombre d’itérations (5,10,15,...) le fichier. Cependant, encoder trop de fois le fichier pouvait
mener à un mauvais fonctionnement de ce dernier. Les antivirus sont aujourd’hui
là aussi capables de détecter un fichier, même encodé plusieurs fois avec un encodeur connu.


Ce qui est mis en cause ici est le procédé totalement automatique. En effet, toutes ces techniques pouvaient
marcher il y a quelques années, mais marchent de moins en moins et aujourd’hui il
est quasiment impossible de créer un virus indétectable des antivirus en un seul clic. Cela pourra fonctionner
si la machine visée n’a pas d’antivirus installé (ce qui est très rare de nos
jours) ou alors qu’elle est très ancienne avec un antivirus qui n’a pas été mis à jour depuis plusieurs années.


Aujourd’hui pour créer un virus qui ne devienne pas détectable des antivirus, il faut mettre les mains dans le
cambouis ! La première technique serait de modifier le corps du programme avant
qu’il ne soit compilé afin de le rendre unique. Cette technique fait toujours ses preuves et moitié moins
d’antivirus détectent la menace.

Une autre technique serait de tenter de stopper l’antivirus lors de l’exécution du virus, ainsi il ne sera pas
possible de détecter la menace.


Encoder soi-même le virus serait aussi une solution. Si nous n’utilisons pas un encodeur connu, le fichier deviendra
difficilement détectable par un antivirus, car il ne l’aura jamais rencontré
auparavant.


Une dernière solution pour passer outre les vérifications des antivirus serait de totalement coder un virus
soi-même de bout en bout. Cette technique sera la plus complexe et la plus longue,
mais sera certainement celle qui apportera le plus de résultats positifs. En effet, les antivirus ne pourront ni
utiliser leur méthode de reconnaissance par signature, ni l’analyse statique,
ni l’analyse heuristique qui sont les trois techniques de reconnaissances majoritairement utilisées par les
meilleurs antivirus que l'on connaît actuellement.


Pour conclure, les méthodes de création d’antivirus en appuyant sur un bouton ne fonctionne quasiment plus
aujourd’hui pour les antivirus les plus connus et les plus utilisés
(Windows defender, Bitdefender, Avast, ...) car ces derniers ont développé au cours des dernières années des
techniques puissantes de reconnaissance de programmes malveillants. Ce genre
de méthode pourrait néanmoins fonctionner sur des machines anciennes et non mises à jour depuis plusieurs
années. Les méthodes de bypass d’antivirus nécessitent aujourd’hui de bonnes
connaissances en informatique (en logiciel, en réseaux et en programmation) et un temps assez long de
développement.


Ainsi, tromper un antivirus est possible et il faut rester vigilant, mais créer un virus qui tromperait des
antivirus n’est pas donné à tout le monde.


Sources :

Vidéo YouTube qui présente très bien tous ces problèmes : [voir la vidéo Youtube](https://www.youtube.com/watch?v=2H_1ZkZ83gI&t=131s)
