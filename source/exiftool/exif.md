# Exiftool

## Cours

### Qu'est ce qu'Exiftool ?

Exiftool est un outil en ligne de commande pour lire, écrire et éditer les métadonnées de différents types de fichiers différents.

### Qu'est ce les Métadonnées ?

Lorsque vous prenez une photo avec votre smartphone, vous pouvez la retrouver et la visioner dans votre gallerie d'images dès que vous voulez. Votre smartphone ne prend cependant pas uniquement une capture de l'instant. En effet, ce dernier capture la date et l'heure précise à laquelle vous appuyez sur le bouton pour prendre votre photo, ajoute à cela la taille de résolution de l'image, la position gps, et plein d'autres informations supplémentaires qui sont ajoutées à l'image. Toutes ces informations sont appelées les métadonnées.

### Comment visionner les Métadonnées d'une image ?

Exiftool vous permet très facilement de lire ces métadonnées de vos photos : 

```shell
    exiftool <image.jpg>
```

### Pourquoi les Métadonnées sont importantes dans le monde de la cybersécurité ?

Lorsque vous envoyez une image à un proche, vous l'envoyez avec toutes ses Métadonnées. Si l'image d'origine est interceptée ou dérobée par une personne malveillante, cette dernière pourra lire les métadonnées de l'image. Ayant précisé juste avant que l'image pouvait contenir des coordonnées GPS exactes, vous pouvez imaginer ce qu'une personne malveillante peut faire. Le modèle d'appareil qui a pris la photo peut aussi être identifié, ce qui peut être utile dans la phase de reconnaissance pour une future exploitation de failles, en connaissant le modèle de l'appareil à infecter la tâche s'annonce tout de suite plus simple pour un attaquant.
Ainsi, même si l'image n'est pas compromettante en elle même, elle peut le devenir par ses métadonnées.

### Détails compatibilité

Vous pouvez retrouver tous les types de fichiers compatibles avec exiftool sur le site officiel : [exiftool.org](https://exiftool.org/)

## Challenge

### Trouver le pseudo de l'artiste de l'image suivante : 

![image exif](./images/exifimg.jpg)

### Source image : 
L'image a été trouvée sur le site : 
[freepng.com](https://en.freejpg.com.ar/free/info/100031658/milky-way-pine-forest-night-dawn)
puis les métadonnées ont été modifiées pour ce challenge.