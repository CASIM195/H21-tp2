# TP2 - Énoncé

:calendar: **À remettre pour le 3 mars 2021 à 22h**

## Objectifs

- Utiliser des outils de planification et de gestion efficacement et de façon organisée
- Gérer les exceptions du code
- Renvoyer des exceptions HTTP formattées
- Créer des tests unitaires et E2E
- Ajouter des nouvelles fonctionnalités à partir de récits utilisateurs

## Partie 1 - Outils de planification (30%)

**Avant** d'entamer la programmation, nous vous demandons de lire attentivement les exigences de la **partie 2**. Nous vous demandons ensuite de planifier vos tâches *de développement logiciel* avec **Github**. 

1. :scroll: **Créez un *milestone*** pour la remise du tp. Insérez une capture d'écran afin de montrer les informations du milestone ainsi que les issues qu'il contient.
2. :scroll: **Créez des *issues*** afin de suivre votre progrès et de vous séparer la tâche. :warning: **Attention** Ce n'est pas nécéssairement 1 issue pour 1 feature. Assurez-vous également d'y remplir l'ensemble des parties tel que vu en laboratoire (l'issue doit au moins être en cours). Insérez une capture d'écran par issue (MAX 3). 
3. :scroll: **Créez des *PRs*** afin de suivre les changements effectués ou en attente. Assurez-vous également d'y remplir l'ensemble des parties tel que vu en laboratoire. Insérez une capture d'écran par PRs **une fois résolue** (MAX 3). Vous n'avez pas à *scroller* afin de montrer le contenu des activités et commentaires.
4. :scroll: **Créez un *Github Project*** contenant vos issues. Insérez une capture d'écran montrant le tableau résultant. Elle peut être effectuée au début comme à la fin de votre progrès. Nous devons au moins y voir les colonnes ainsi que quelques issues. Une seule capture suffit (pas besoin de *scroller*).

## Partie 2 - Code (40%)

Pour cette partie, vous devrez développer les features demandées. Les formats de requêtes et réponse utilisent la notation typée de Typescript. **On s'attend à une réponse dans le format JSON pour l'ensemble des appels à l'API**. Des tests automatisés vérifieront les bons retours de votre API. Nous corrigerons également la **clarté** (clean code), l'**organisation** et l'**uniformisation** du code.

De plus, à partir de ce TP, vous devez gérer les exceptions et retourner les réponses demandées. Le format global de toutes les exceptions est [**décrit ICI**](./features/exceptions.md).

:warning: **Attention**: Les features 1 et 2 ont été modifiées (incluant les payloads!). Assurez-vous de bien les mettre à jour en suivant les nouvelles descriptions!

### Features

- [Feature 1 (modifiée)](./features/feature1-maj.md)
- [Feature 2 (modifiée)](./features/feature2-maj.md)
- [Feature 3](./features/feature3.md)
- [Feature 4](./features/feature4.md)
- [Feature 5](./features/feature5.md)

## Partie 3 - Tests (30%)

Pour cette partie, on vous demande de tester chaque appel à votre API, selon votre méthode préférée. Ces tests doivent inclure, pour **chaque** route d'API:

- Les appels réussis
- Les appels erronés
- Les payloads
- Les code d'erreur
- Les status HTTP

De plus, on s'attend à ce que l'ensemble des classes *logiques* soient testées unitairement, c'est-à-dire :

- Les factories
- Les assemblers
- Les implémentations de repositories
- Les value objects (ex: ids, amount, etc.)
- Toute autre classe effectuant une certaine logique (transformation, action, calcul, copiage, validation, etc.)

> Pour ceux étant plus avancés, on ne s'attend **pas** à des tests d'interactions (aka avec des Mocks et des `verify`). 