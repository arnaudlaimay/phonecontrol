# phonecontrol
Arnaud LAIMAY 

Enoncé : 

idée 2_ Créer un synthétiseur controlé directement par les mouvements d’un smartphone 

Description projet :


Je souhaite utiliser un logiciel appelé « GyrOSC » qui permet d’extraire des données des capteurs d’un téléphone. Je pensais par exemple intéressant de contrôler un synthétiseur FM (créer dans pure data par exemple) seulement à partir de l’orientation et des mouvements d’un téléphone. Le synthétiseur pourrait être aussi controlé via une application type Touch OSC.
C’est la dessus j’axe ma recherche en ce moment et le projet me parait réalisable.

Analyse des besoins :

Un téléphone sera nécessaire avec l’application Touch OSC et GyrOSC.
Le téléphone enverra des données par message OSC pour contrôler un synthétiseur créer sur Pure Data. Celui-ci aura surement des traitements audio additionnels comme de la reverb ou autres.
(Smartphone, GyrOSC, Touch OSC, Ordinateur, Pure Data, Clavier Midi)


Acquisition de connaissances :

Je regarde en ce moment ce qui se fait en terme d’application sur téléphone ainsi que sur les informations que je peux extraire des capteurs d’un smartphone. Je réfléchis aussi à la composition et à la configuration que je souhaite pour le synthétiseur.
D’autres part je dois trouver comment pure data va bien interpréter les données reçues en OSC pour contrôler les différents paramètres.

Modèle :
iPhone équipé de l’application GyrOSC + (Touch OSC)
Clavier Midi

Messages OSC

Son avec effet
HP
Pd Synth +
Effets audio
Patch Pure data qui reçoit OSC
Interface audio
Ordinateur

Méthode :
Je vais tout d’abord me familiariser avec la transmission de messages OSC d’un téléphone vers Pure Data. Ensuite je vais voir quels mouvements du téléphone sont pertinents pour le projet. En parallèles j’élaborerais un patch Pure Data avec un synthétiseur puis quelques effets.


ETAPE 2

Je suis entrain de confectionner deux patch pure data. L’un me permettant de recevoir les informations d’orientation du téléphone : pour l’instant Pitch, Yaw et Roll (via GyrOSC). Le deuxième relie ses données reçus pour les « Mapper » sur un synthétiseur avec effets. 
En parallèle je relie aussi TouchOSC avec le patch. 

Les patch nécessite plusieurs bibliothèque d’objet pure data : cyclone, iemlib, comport etc...

La communication entre le téléphone et pure data fonctionne bien. Je dois ajuster l’échelle des valeurs pour ne pas que cela devienne cacophonique. Il me reste aussi a perfectionner le système et ajouter une meilleur structure de contrôle d’effet.
D’autre part je réfléchis à la manière avec laquelle je vais pouvoir créer des notes directement à partir du téléphone.
