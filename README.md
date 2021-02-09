# TP2 - Énoncé

:calendar: **À remettre pour le 3 mars 2021 à 22h**

## Objectifs

- Utiliser des outils de planification et de gestion efficacement et de façon organisée
- Gérer les exceptions du code
- Renvoyer des exceptions HTTP formattées
- Créer des tests unitaires et E2E
- Ajouter des nouvelles fonctionnalités à partir de récits utilisateurs

## Partie 1 - Outils collaboratifs (10%)

1. En équipe, choisissez une convention de _check style_ (_linting_) qui convient à tous.
2. Configurez-la dans IntelliJ afin d'activer le formattage automatique.
3. Ajoutez l'étape de _checkstyle_ dans le cycle de vie Maven.

## Partie 2 - Outils de planification (20%)

**Avant** d'entamer la programmation, nous vous demandons de lire attentivement les exigences du tp. Nous vous demandons ensuite de planifier vos tâches _de développement logiciel_ avec **Github**.

1. :scroll: **Créez un _milestone_** pour la remise du tp. Insérez une capture d'écran afin de montrer les informations du milestone ainsi que les issues qu'il contient.
2. :scroll: **Créez des _issues_** afin de suivre votre progrès et de vous séparer la tâche. :warning: **Attention** Ce n'est pas nécéssairement 1 issue pour 1 feature. Assurez-vous également d'y remplir l'ensemble des parties tel que vu en laboratoire (l'issue doit au moins être en cours). Insérez une capture d'écran par issue (MAX 3).
3. :scroll: **Créez des _PRs_** afin de suivre les changements effectués ou en attente. Assurez-vous également d'y remplir l'ensemble des parties tel que vu en laboratoire. Insérez une capture d'écran par PRs **une fois résolue** (MAX 3). Vous n'avez pas à _scroller_ afin de montrer le contenu des activités et commentaires.
4. :scroll: **Créez un _Github Project_** contenant vos issues. Insérez une capture d'écran montrant le tableau résultant. Elle peut être effectuée au début comme à la fin de votre progrès. Nous devons au moins y voir les colonnes ainsi que quelques issues. Une seule capture suffit (pas besoin de _scroller_).

## Partie 3 - Code (30%)

Pour cette partie, vous devez développer les features demandées. Les formats de requêtes et réponses utilisent la notation typée de Typescript. **On s'attend à une réponse dans le format JSON pour l'ensemble des appels à l'API**. Des tests automatisés vérifieront les bons retours de votre API. Nous corrigerons également la **clarté** (clean code), l'**organisation** et l'**uniformisation** du code.

De plus, à partir de ce TP, vous devez gérer les exceptions et retourner les réponses demandées. Le format global de toutes les exceptions est [**décrit ICI**](./features/exceptions.md).

### Features

- [Exceptions](./features/exceptions.md)
- [Feature 1 (v2)](./features/feature1-v2.md)
- [Feature 3](./features/feature3.md)
- [Feature 4](./features/feature4.md)
- [Feature 5](./features/feature5.md)

## Partie 4 - Tests (30%)

Pour cette partie, on vous demande de tester chaque appel à votre API, selon votre méthode préférée (_Rest-Assured_, _Postman_, etc.). Vous devez donc tester, pour **chaque** route d'API:

- Les appels réussis
- Les appels erronés
- Les payloads
- Les codes d'erreur
- Les status HTTP

De plus, on s'attend à ce que l'ensemble des classes _logiques_ soient testées unitairement, c'est-à-dire :

- Les factories
- Les assemblers
- Les entites
- Les implémentations de repositories
- Les value objects (ex: ids, amount, etc.)
- Toute autre classe effectuant une certaine logique (transformation, action, calcul, copiage, validation, etc.)

**Détails**:

- Vous pouvez omettre les tests de Resources puisque vous aurez fait des tests E2E.
- Pour ce TP, vous pouvez également omettre les tests de UseCases puisqu'ils forment plutôt des tests fonctionnels et d'intégrations. Ceux-ci seront vu dans un prochain TP.
- Pour ceux étant plus avancés, on ne s'attend **pas** à des tests d'interactions (aka avec des Mocks et des `verify`).

## Partie 5 - Intégration continue (10%)

Maintenant que des tests de qualité sont en place, vous pouvez avoir la confiance de pratiquer l'intégration continue. Ainsi, on vous demande de mettre en place un _workflow_ Github Actions vous permettant d'automatiser vos tests. Votre _workflow_ **doit au moins** comprendre les tâches suivantes :

1. Linting
2. Compilation
3. Unit-tests
4. E2E tests

Vous devez également déterminer le nombre de _jobs_ qui sont nécéssaires ainsi que leurs dépendances.
