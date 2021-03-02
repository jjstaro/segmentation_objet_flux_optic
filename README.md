# Segmenation des objects en se basant sur le flot optique
 
 Cet travail est un Travail pratique sur la Vision par ordinateur. Il est divisé en deux grandes parties : 
 
 ## 1- L'Estimation du flot optique dans une séquence d'images
 Pourla première partie de ce tp, nous allez calculons le flot optique dense d'une séquence d'images.
 Pour cela nous utilisons les fonctions déjà implémentées dans la bibliothèque OpenCV à savoir la fonction
 **cv.calcOpticalFlowFarneback()** permets de cal culer le flot optique dense. 
 **Reférence :** https://docs.opencv.org/3.4/d4/dee/tutorial_optical_flow.html
 Pour chaque frame d'une vidéo, nous estimons le flot optique de ce frame en nous basant sur le frame
 courrent et le frame précédant. A chaque pixel du frame, nous avons un vecteur de vitesse ( flot optiq ue)
 dont l'angle (direction) et la norme peuvent être détermines. 
 Ensuite nous utiliserons ces valeurs dans la deuxième partie. Nous visualiserons la norme en créant une image dont la valeur du pixel est la norme
 de son flot optique . Nous convertirons ces valeurs en nombre entier entre 0 et 255. 

 ## 2- La segmentation des ogjets en mouvement
Dans une video, si des objets bougent à différentes vitesses, les normes du flot optique sont aussi
différentes. S'ils se bougent d ans d es d ir ectio ns différentes l es flot s optiq ue s d e c es objets ont des
différents angles Donc, le flot o ptique la n orme ou l'ange ou l es d eux) vous aide à segmenter d es
objets en mouvement en appliquant une méthode de segmentation que nous avons seuillage, k
means,
Pour le premier essai, nous segmenteons les objets se deplaçant le plus vite en appliquant le seuillage
sur les normes du flot optique. Ensuite, nous utilisons plusieurs seuils pour segmenter des objets à
différentes vitesses. Pour rafinner les résultat, supprimerons les les les petites régions facultatives en
jouant sur l'effet d es paramètres.

Pour améliorer le résultat de segmentation, nous profiterons de l'angle du flot optique . 
Nous choisirons aussi d'autre méthode segmentation que nous appliqerons sur la norme ou etl'ang le du flot optique. 
Nous ferons l'analyse et la comparaison des résultats obtenus avec des différentes méthodes ou des types de données (norme, angle ou les deux)
