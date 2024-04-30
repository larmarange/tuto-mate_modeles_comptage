# Modèles de comptage · Tuto@Mate · mai 2024

Présentation sur les modèles de comptage réalisée dans le cadre des Tuto@Mate le 21 mai 2024.

## Ressources sur guide-R

- https://larmarange.github.io/guide-R/analyses_avancees/modeles-comptage.html
- https://larmarange.github.io/guide-R/analyses_avancees/modeles-incidence.html
- https://larmarange.github.io/guide-R/analyses_avancees/modeles-zero-inflated.html

## Résumé

Les modèles de comptage permettent de modéliser un nombre entier correspondant le plus souvent au nombre d'occurrences d'un événement (par exemple un nombre d'enfants, ou bien un nombre de cas positifs).  Pour expliquer une variable de ce type, les modèles linéaires ou les régressions logistiques ne sont pas adaptées. On aura alors recours à des modèles ou régressions de Poisson, c’est-à-dire de manière plus spécifique à un modèle linéaire généralisé (GLM en anglais), avec une fonction de lien logarithmique et une distribution statistique de Poisson.

Les modèles de Poisson font l’hypothèse que la variance est égale à la moyenne, ce qui ne s’observe pas toujours. Auquel cas on aura alors un problème de surdispersion. Dans ce cas-là, nous pourrons avoir recours à des modèles apparentés aux modèles de Poisson, à savoir les modèles quasi-Poisson et les modèles binomiaux négatifs.

Les modèles de comptage peuvent aussi être utiliser pour un outcome binaire, en lieu et place d’une régression logistique, afin d’estimer des prevalence ratios plutôt que des odds ratios.

Les modèles de comptage peuvent également être utilisés pour des modèles d'incidence ou de taux, en rapportant un nombre d'événements à une durée d'exposition.

Enfin, lorsqu’il y a un nombre important de 0 dans les données à expliquer, on peut avoir recours à des modèles zero-inflated ou des modèles hurdle qui, d’une certaine manière, combinent deux modèles en un (d’une part la probabilité de vivre l’évènement et d’autre part le nombre d’occurrences de l’évènement).
