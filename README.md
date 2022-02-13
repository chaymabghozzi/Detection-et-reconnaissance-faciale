# detection-et-reconnaissance-faciale

Solution 1 : Utilisation de la bibliothèque OpenCV et l’algorithme LBPH

✦ La Détection de visage avec OpenCV :

Notre système permet de réaliser la détection faciale sur un fichier vidéo sauvegardé sur le disque
dur. Il examine les composantes de chaque image et classe les objets détectés. Nous avons utilisés
le fichier haarcascade_frontalface_default.xml pour la détection des visages.

Solution 2 : Utilisation des bibliothèques Dlib et OpenCV avec Landmarks

Notre objectif est de détecter les structures faciales importantes sur le visage à l’aide de méthodes de
prédiction de forme.

✦ Capture d’image :
Pour plus de commodité, nous avons utilisé la bibliothèque OpenCV sur une vidéo sauvegardée
sur le disque dur pour capturer des images.

✦ Détection des visages :
La détection de visage est la première méthode qui localise un visage humain et renvoie une
valeur en x,y,w,h qui est un rectangle.
Dlib utilise les méthodes HOG (Histogramme des Gradients Orientés) et SVM (Support Vector
Machine) pour la détection.

✦ Projection des visages :
Après isolation des visages, nous devons résoudre le problème des visages tournés en différentes
directions. Alors, nous essayons de déformer chaque image de sorte que les yeux et les lèvres soient
toujours à en face dans l’image. Pour appliquer cette déformation nous avons utilisé l’algorithme
« Face Landmark Estimation » qui utilise le modèle :
« Le modèle de repère 68-face de Dlib » (shape_predictor_68_face_landmarks.dat)
pour trouver 68 points spécifiques appelé points de repère du visage, le haut du menton, le bord
extérieur de chaque œil, le bord intérieur de chaque sourcil, etc

✦ Trouver le nom de la personne à partir de l’encodage :
Pour faciliter ce processus nous avons utilisé le modèle de reconnaissance faciale «Face Recognition»
(dlib_face_recognition_resnet_model_v1.dat) Ce modèle permet d’assurer la reconnaissance
faciale dans un temps record en utilisant notre modèle qui a une précision de 99,38
