# Resolution-Numerique-EDO-EDS

# Méthodes Numériques : Lotka-Volterra et Black-Scholes

Ce dépôt contient l'implémentation en Python de méthodes numériques appliquées à la résolution d'équations différentielles ordinaires (EDO) et stochastiques (EDS), réalisé dans le cadre d'un TP noté et a obtenu la note de 17/20.

## 📋 Description du projet

Le projet est divisé en deux parties distinctes :

### 1. Modèle de dynamique des populations (Lotka-Volterra)
Étude de l'évolution d'un système proie-prédateur à l'aide de différents schémas numériques :
* Implémentation des schémas d'**Euler Explicite** et de **Heun**.
* Tracé des trajectoires temporelles $x(t)$ et $y(t)$ ainsi que du portrait de phase $(x_n, y_n)$.
* Analyse de la conservation de la quantité $H(x,y)$ au cours du temps selon le schéma utilisé.
* Étude de la convergence du schéma de Heun par rapport à une solution de référence (`scipy.integrate.solve_ivp` avec la méthode `RK45`), confirmant un ordre de convergence d'environ 2.

### 2. Modèle de Black-Scholes et Pricing par Monte Carlo
Application des probabilités numériques à la finance :
* Simulation de 20 trajectoires de l'actif $S_t$ avec le schéma d'**Euler-Maruyama**.
* Pricing d'une option Call par la méthode de Monte Carlo.
* Comparaison avec le prix théorique de Black-Scholes et calcul de l'intervalle de confiance (à 95%).
* Analyse de la convergence forte/faible en évaluant l'évolution de l'erreur relative en fonction du nombre de pas de temps $N$.

## 🛠️ Technologies et Librairies utilisées

Ce projet a été développé initialement sur Google Colab et requiert les librairies Python suivantes :
* `numpy` : Pour le calcul matriciel et la génération de nombres aléatoires (incréments gaussiens).
* `matplotlib.pyplot` : Pour la visualisation des trajectoires, des portraits de phase et des erreurs de convergence.
* `scipy` (`scipy.integrate`, `scipy.stats`) : Pour les solveurs d'EDO de référence et la fonction de répartition de la loi normale

