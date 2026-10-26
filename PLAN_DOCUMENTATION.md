# Plan des fichiers et dossiers

## Objectif

Ce plan propose une organisation progressive des livrables de l’équipe sur les
risques d’architecture, la sécurité, l’hébergement, les évolutions
technologiques et les normes et réglementations applicables au service de
gestion de jeux en ligne.

Les dossiers et fichiers ci-dessous sont une cible de documentation. Ils ne
sont pas tous créés tant que leur contenu n’a pas été rédigé.

## Arborescence cible

```text
.
├── README.md
├── PLAN_DOCUMENTATION.md
└── docs/
    ├── 01-cadrage/
    │   ├── contexte-et-perimetre.md
    │   ├── parties-prenantes-et-hypotheses.md
    │   └── actifs-et-donnees.md
    ├── 02-architecture-hebergement/
    │   ├── architecture-cible.md
    │   ├── flux-et-frontieres-de-confiance.md
    │   ├── hebergement-et-services-tiers.md
    │   └── disponibilite-sauvegarde-reprise.md
    ├── 03-risques/
    │   ├── methode-et-echelles.md
    │   ├── registre-des-risques.md
    │   └── scenarios-et-traitements.md
    ├── 04-securite/
    │   ├── exigences-de-securite.md
    │   ├── identites-et-controles-d-acces.md
    │   ├── securite-applicative-et-api.md
    │   ├── protection-des-donnees.md
    │   └── supervision-et-gestion-des-incidents.md
    ├── 05-evolutions-technologiques/
    │   ├── veille-et-hypotheses.md
    │   ├── analyse-des-impacts.md
    │   └── mesures-d-anticipation.md
    └── 06-normes-reglementations/
        ├── registre-des-exigences.md
        ├── protection-des-donnees.md
        ├── cybersecurite-et-services-numeriques.md
        └── paiements-et-jeux-reglementes.md
```

## Contenu attendu par dossier

### `01-cadrage/` — contexte et limites

- **`contexte-et-perimetre.md`** : objectifs du service, fonctions concernées,
  inclusions, exclusions et périmètre de l’équipe.
- **`parties-prenantes-et-hypotheses.md`** : utilisateurs, exploitant,
  fournisseurs, responsables de décision, hypothèses et questions ouvertes.
- **`actifs-et-donnees.md`** : comptes, données personnelles, données de jeu,
  contenus, secrets, journaux et autres actifs à protéger ; préciser les
  classifications et durées de conservation lorsqu’elles sont connues.

### `02-architecture-hebergement/` — conception et exploitation

- **`architecture-cible.md`** : composants, responsabilités, environnements et
  schéma d’architecture.
- **`flux-et-frontieres-de-confiance.md`** : flux de données, interfaces,
  protocoles, points d’entrée et frontières de confiance.
- **`hebergement-et-services-tiers.md`** : modèle d’hébergement, responsabilités
  partagées, dépendances, localisation et risques fournisseurs.
- **`disponibilite-sauvegarde-reprise.md`** : objectifs de disponibilité,
  sauvegardes, restauration, continuité et reprise après sinistre.

### `03-risques/` — analyse et suivi

- **`methode-et-echelles.md`** : méthode d’évaluation, échelles de vraisemblance
  et d’impact, critères d’acceptation et règles de mise à jour.
- **`registre-des-risques.md`** : identifiant, scénario, actif ou objectif
  touché, causes, conséquences, vraisemblance, impact, niveau, propriétaire,
  traitement, échéance et risque résiduel.
- **`scenarios-et-traitements.md`** : scénarios prioritaires et justification
  des mesures de réduction, transfert, évitement ou acceptation.

### `04-securite/` — mesures de protection

- **`exigences-de-securite.md`** : exigences transverses et critères de
  vérification.
- **`identites-et-controles-d-acces.md`** : authentification, autorisations,
  privilèges, comptes d’administration et gestion du cycle de vie des comptes.
- **`securite-applicative-et-api.md`** : conception sécurisée, validation des
  entrées, gestion des sessions, protections des API et gestion des
  vulnérabilités.
- **`protection-des-donnees.md`** : minimisation, chiffrement, gestion des
  secrets, accès, conservation et suppression.
- **`supervision-et-gestion-des-incidents.md`** : événements à journaliser,
  alertes, responsabilités, escalade, réponse et retour d’expérience.

### `05-evolutions-technologiques/` — veille et adaptation

- **`veille-et-hypotheses.md`** : technologies et évolutions surveillées, sources
  et horizon de veille.
- **`analyse-des-impacts.md`** : bénéfices, nouvelles dépendances, menaces,
  impacts sur les compétences, coûts, données et conformité.
- **`mesures-d-anticipation.md`** : critères d’adoption, tests, garde-fous,
  plans de retour arrière et réévaluation des risques.

### `06-normes-reglementations/` — obligations et référentiels

- **`registre-des-exigences.md`** : exigence, source officielle, juridiction,
  condition d’applicabilité, éléments de preuve, responsable et état.
- **`protection-des-donnees.md`** : analyse des obligations de protection des
  données personnelles et des mesures de conformité pertinentes.
- **`cybersecurite-et-services-numeriques.md`** : analyse conditionnelle des
  textes de cybersécurité et des règles applicables aux services numériques.
- **`paiements-et-jeux-reglementes.md`** : analyse à compléter uniquement si le
  service comporte des paiements ou des fonctionnalités relevant des jeux
  d’argent et de hasard réglementés.

## Ordre de rédaction recommandé

1. Valider le contexte, les frontières du périmètre et les hypothèses.
2. Inventorier les actifs, les données, les acteurs et les services tiers.
3. Décrire l’architecture, l’hébergement et les flux.
4. Définir la méthode puis construire le registre des risques.
5. Déduire et documenter les mesures de sécurité et de continuité.
6. Évaluer les évolutions technologiques et leurs impacts.
7. Vérifier l’applicabilité des textes et référentiels à partir de sources
   officielles, puis relier chaque exigence aux mesures et preuves attendues.
8. Réviser le registre et les décisions à chaque évolution importante du service.

## Règles de rédaction et de maintenance

- Dater les analyses et indiquer leur auteur ou leur responsable.
- Distinguer faits confirmés, hypothèses et décisions en attente.
- Associer les risques et exigences à des responsables et à des actions
  vérifiables.
- Citer les sources officielles et noter la date de consultation ; ne pas
  présenter une piste réglementaire comme une obligation confirmée sans analyse
  d’applicabilité.
- Ne pas publier de secrets, d’identifiants, de données réelles d’utilisateurs
  ou de détails opérationnels sensibles dans les documents.
- Réexaminer les documents lorsque l’architecture, les fournisseurs, les
  juridictions, les données traitées ou les fonctionnalités changent.
