[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1qq7IMBIjbWDH6TlOSNbSJuucBWL73ips#scrollTo=ZvgJuVNPT2ck)

# Project_ResNets
Projet final Deep Learning : Deep Residual Learning for Image Recognition 


L'objectif de ce projet a été de reporduire les résultats clés de l'article en s'intéressant au mécanisme des connexions résiduelles et en cherchant à faire une exploration sur différents spécificités de l'architecture. 

Contenu du Repository
paper/ : L'article original de Kaiming He et al.
ResNets.py : le notebook d'exploration du concept de ResNets
slides/ : Présentation sytnthétique des résultats
results/ : Graphiques de perte (loss) et précision (accuracy) générés


Le Concept : ResNetLes réseaux de neurones très profonds souffrent d'un problème de dégradation : ajouter des couches augmente l'erreur d'entraînement, non pas à cause du surapprentissage, mais à cause de difficultés d'optimisation.La solution : L'apprentissage résiduel. Au lieu d'apprendre une fonction $H(x)$, on force le réseau à apprendre le résidu $F(x) = H(x) - x$ grâce à des "shortcut connections" (connexions raccourcies).


 Méthodologie : J'ai mené mes expériences sur le dataset CIFAR-10, en suivant le protocole décrit dans la section 4.2 de l'article :Architecture : Comparaison entre réseaux "Plain" (simples) et "ResNet" (résiduels).Profondeurs testées : 20 couches et 56 couches ($n=3$ et $n=9$).Pré-traitement : Normalisation et Data Augmentation (padding, random crop, flip).


Expérience & Résultats1. Reproduction des résultats (Baseline)Comparaison de l'erreur d'entraînement et de test au fil des époques.Plain-56 vs Plain-20 : Le réseau plus profond (56) performe moins bien que le réseau superficiel (20), confirmant le problème de dégradation.ResNet-56 vs ResNet-20 : Le ResNet-56 surpasse le ResNet-20, prouvant l'efficacité des connexions résiduelles.(Assure-toi de mettre ton image png générée ici)2. 


Partie Exploratoire : [Titre de ton idée, ex: Impact de la Batch Norm]Une extension au-delà de la reproduction simple.Hypothèse : [Ex: La Batch Normalization est indispensable pour que le résidu fonctionne].Observation : [Ex: Sans BN, le modèle diverge immédiatement].


Références
- **Article Original :** He, K., Zhang, X., Ren, S., & Sun, J. (2016). Deep Residual Learning for Image Recognition. *CVPR*. [Lien PDF](https://arxiv.org/pdf/1512.03385.pdf)
- **Dataset :** [CIFAR-10](https://www.cs.toronto.edu/~kriz/cifar.html) 



