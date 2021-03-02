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
