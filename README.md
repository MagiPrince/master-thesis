# Thèse de travail de master

Il s'agit de ma thèse de travail de master intitulée : __Détection rapide de jets basée sur l'apprentissage automatique pour le traitement en temps réel sur FPGA au sein de l'expérience ATLAS au LHC__.

Résumé :

Dans le cadre de l'expérience ATLAS au sein du LHC au CERN, des particules entrent en collision toutes les 25 ns générant environ 25 MB de données. De par la fréquence élevée de ces événements et la quantité de données en résultant, il est indispensable de conserver uniquement les interactions intéressantes. Afin d'effectuer cette sélection en temps réel, un système de déclenchement à deux niveaux a été mis en place. Le premier est caractérisé par une très faible latence, de moins de 2.5 ms, implémenté sur de l'électronique dédiée et sur des FPGA. Le second effectue des analyses détaillées de chaque collision dans de grandes fermes de processeurs. La fréquence initiale de 40 MHz peut ainsi être diminuée à 100 kHz puis à 1 kHz. Parmi les données traitées, celles contenant des jets sont utilisées s'ils sont présents en grand nombre, ou s'ils sont très énergétiques. Ceux-ci résultent de processus complexes, et sont habituellement observés suite à une collision entre protons.

Le but de ce travail de master est de développer un algorithme d'apprentissage automatique pour la reconstruction de jets en temps réel sur FPGA. Pour ce faire, le modèle YOLOv8, étant à la pointe pour les tâches de vision par ordinateur, est utilisé et évalué dans un premier temps, puis une version modifiée du réseau de neurones ResNet18 capable de réaliser de la détection, choisi pour son architecture relativement simple, est développé et évalué en Keras, quantifié avec QKeras, puis finalement synthétisé sur FPGA à l'aide de l'outil HLS4ML. L'ensemble du projet contribue dans la recherche d'algorithmes de détection de jets en temps réel et de leur implémentation sous-jacente dans des systèmes à faible latence, en proposant l'évaluation à différents niveaux de deux réseaux neuronaux convolutifs pour cette tâche. 

Ce travail a mené à trois contributions ; le processus de développement complet de ResNet18+Tête pour une implémentation sur FPGA, la représentation de données complexes sous forme d'images, et la réalisation d'une procédure pour utiliser efficacement HLS4ML.