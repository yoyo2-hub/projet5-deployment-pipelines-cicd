# projet5-deployment-pipelines-cicd

## Automatiser le déploiement Power BI avec Deployment Pipelines

**Domaine :** DevOps, ALM & CI/CD — **Product Owner :** PO 3

---

## 1. Besoin métier

Une fois qu'un rapport Power BI a été modifié et validé en développement, il faut le faire avancer vers les utilisateurs finaux de façon fiable — sans copier-coller manuel source d'erreurs, sans casser la production, et avec la possibilité de revenir en arrière en cas de problème. Ce projet répond à ce besoin : **automatiser et sécuriser le passage d'une solution Power BI entre les environnements de développement, de test et de production.**

## 2. Contexte fil rouge

Vous travaillez sur les données de vente de l'entreprise fictive **AdventureWorks** (ventes, clients, produits, magasins, commerciaux) — le même contexte métier que toutes les autres équipes du dispositif.

## 3. Description générale du projet

**Mission :** à partir d'une solution **déjà versionnée**, configurer ou simuler un **processus de déploiement** entre Développement, Test et Production, avec les **Power BI Deployment Pipelines**. Vous devez documenter les étapes du déploiement, les contrôles à effectuer avant la mise en production, les paramètres qui dépendent de l'environnement, et une procédure simple de **retour arrière (rollback)**.

## 4. Comment démarrer

1. **Point de départ :** vous n'avez pas besoin d'attendre le vrai livrable de l'équipe du Projet 4. Simulez vous-même une solution "déjà versionnée" : reprenez ou créez un rapport Power BI simple sur AdventureWorks, convertissez-le en PBIP si besoin, et placez-le dans `pbip/` comme point de départ.
2. Créez 3 workspaces Power BI Service (DEV / TEST / PROD) et reliez-les avec un **Deployment Pipeline**.
3. Identifiez au moins un paramètre qui doit changer selon l'environnement (ex : une source de données ou une chaîne de connexion) et configurez les règles de déploiement correspondantes.
4. Documentez les contrôles que vous effectuez avant chaque passage à l'environnement suivant.
5. Démontrez un scénario de **rollback** : un déploiement qui pose problème, et son annulation.

## 5. Structure du repo

```
projet5-deployment-pipelines-cicd/
├── README.md
├── docs/
│   ├── architecture.md          → schéma du pipeline de déploiement
│   └── note-pedagogique.md      → à remplir au fur et à mesure (voir section 6)
├── pbip/                        → votre point de départ "déjà versionné" (simulé)
├── scripts/                     → scripts d'automatisation du déploiement, si utilisés
└── tests/                       → non utilisé pour ce projet (laisser vide)
```

## 6. Note pédagogique — squelette à remplir

Dans `docs/note-pedagogique.md`, structurez votre note selon ce plan (imposé pour tous les mini-projets du dispositif) :

- Contexte et problématique métier
- Objectifs du mini-projet et périmètre retenu
- Architecture ou principe de fonctionnement de la solution
- Prérequis, données et technologies utilisées
- Réalisation pas à pas et démonstration du résultat
- Difficultés rencontrées et erreurs fréquentes
- Bonnes pratiques et points de vigilance
- Limites de la solution et pistes d'amélioration
- Courte synthèse réutilisable comme base pédagogique

## 7. Livrables attendus

- Une démonstration fonctionnelle du déploiement entre environnements
- Les fichiers/scripts nécessaires à la reproduction (ce repo)
- Un schéma du pipeline de déploiement (`docs/architecture.md`)
- La note pédagogique complète (`docs/note-pedagogique.md`)

## 8. Critères de réussite

- Le scénario métier est compréhensible
- La solution est reproductible
- Les choix techniques sont justifiés simplement
- Le résultat peut être démontré en direct
- Les limites et points de vigilance sont explicités

## 9. Lien avec les autres projets du domaine

- **Projet 4** (`projet4-pbip-git-alm`) travaille le versionning en amont de votre étape de déploiement
- **Projet 21** (`projet21-tests-automatises-nonregression`) ajoute des tests qui devraient idéalement s'exécuter **juste avant** votre étape de déploiement

➡️ Précisez clairement dans votre note pédagogique à quel moment vos contrôles interviendraient par rapport aux tests automatisés de l'équipe du Projet 21.
