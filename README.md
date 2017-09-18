# legis
Projet étudiant de prédiction du __premier tour__ des législatives françaises à partir du __premier tour__ des présidentielles.

Pour rééquilibrer les classes en présence, nous avons fait appel à la librairie "imbalanced-learn" de Guillaume Lemaître, Fernando Nogueira et Christos K. Aridas.
Voir : Imbalanced-learn: A Python Toolbox to Tackle the Curse of Imbalanced Datasets in Machine Learning, http://jmlr.org/papers/v18/16-365

__/!\ Attention :__ souvent par abus de langage, on dira que tel groupe politique "remporte" une circonscription. Les guillemets ne sont pas là pour rien, et lorsqu'on écrit ce genre de choses, cela signifie en réalité que le groupe politique en question arrive premier au premier tour des législatives.
Cela vaut aussi pour les présidentielles. Lorsqu'on dira qu'un groupe est "arrivé premier" à la présidentielle d'une certaine année dans un certain département, on voudra en réalité dire qu'il est arrivé premier au premier tour.