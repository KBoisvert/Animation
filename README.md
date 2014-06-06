Animation
=========

TP1 animation

Instructions pour le fichier style.css contenant 5 animations différentes.  

Peu importe si vous utilisez une seule animation ou plusieurs, il faut configurer les propriétés de départ de la forme ou du texte qui sera animé.  Les propriétés par défaut (couleur, grandeur) sont dans une classe .general qui doit être appliquée à l’objet à animer dans le html.

Propriétés par défaut :
Par défaut les animations sont encadrées dans un carré de 100px par 70px.  J’ai mis un margin de 40px pour laisser de l’espace entre chaque animation.  Le texte est centré horizontalement et le padding-top sert à le centrer verticalement.  La grosseur de la font/texte par défaut est 12px.  Chaque animation est placée dans une <div> avec la classe correspondante.

Animation :
Voici le détail d’une ligne animation si vous désirez changer la durée de l’animation ou ajouter un délais.  Il n’est pas recommandé de modifier les autres attributs. 
-webkit-animation: anim1 3s ease 0s infinite normal;
-webkit : préfixe pour le navigateur
Animation : pour spécifier qu’on veut faire une animation
Anim1 : nom de l’animation qui sera dans le keyframe
3s : durée de l’animation
Ease : variation de l’animation (linear ou ease-in ou out)
0s : délais avant de démarrer l’animation
Infinite : nombre de fois que l’on veut faire rouler l’animation
Normal : si l’animation se fera vers l’avant (normal), l’arrière (reverse) ou les 2 sens (alternate)


Animation 1 : texte qui monte et descend en se déplaçant vers la droite. (mettre classe .ani1 dans html)
Keyframe : deplaceAngle
Propriétés animées : le déplacement (translate), la couleur du texte et du background, espace entre les lettres.
L’animation démarre lorsque la souris passe sur le texte.  La boîte qui s’agrandie vers la droite est animée d’un simple width sur le hover.  Le texte est animé avec le keyframe deplaceAngle.  Les intervales 0%, 60% et 100% ramènent le texte à sa position initial.  40% envoie le texte vers le haut et 80% vers le bas.

Animation 2 : cercle qui flash (mettre classe .ani2 dans html)
Keyframe : flash
Propriétés animées : la grosseur (scale), la couleur du texte et du background, opacité
Dans le css de base, changer le border-radius pour changer la forme.  J’ai ajouté un margin étant donné que le forme s’agrandie et qu’elle venait en conflit avec les autres formes autour.  L’animation se fait à l’envers (reverse)  elle peut être fait dans les 2 sens ou vers l’avant en changeant le reverse dans le : 	-webkit-animation:anim2 2s ease-in 0s infinite reverse; contre alternate (2 sens) ou normal (avant).

Animation 3 : la forme change dans les 2 sens soit un carré qui devient un parallélogramme (mettre classe .ani3 dans html)
Keyframe : parallele
Propriétés animées : la forme (skew), les bordures de côtés, largeur (width)
L’animation des bordures peut se changer avec la propriété border-left ou right.  Pour changer la forme changer le degré de skew.

Animation 4 : fait comme une vague ou un bateau sur l’eau (mettre classe .ani4 dans html)
Keyframe : vague
Propriétés animées : déplacement (translate), angle (rotate), couleur du texte ou de fond, grosseur du texte, ombre du texte.
Pour faire un effet vague il est nécessaire d’avoir plusieurs translate.  Entre chaque déplacement l’angle a été changé pour donner un effet de vague, peut être changé dans la propriété rotate.

Animation 5 : comme un poisson qui saute de l’eau et fait un tour de 360deg (mettre classe .ani5 dans html)
Keyframe : monteTourne
Propriétés animées : le déplacement (translate),  la rotation (rotate), les bordures, couleurs de fond et du texte
Il est important de garder un angle plus grand que 360deg après la rotation complète.  Pour changer la hauteur il faut changer la deuxième valeur du translate.
