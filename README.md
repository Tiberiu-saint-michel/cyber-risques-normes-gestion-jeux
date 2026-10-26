# Gestion de jeux en ligne — risques, sécurité et conformité

## Présentation

Ce projet documente la conception et l’hébergement d’un service de gestion de
jeux en ligne, du point de vue de notre équipe. Il porte sur les risques
associés à l’architecture et à l’exploitation, les mesures de sécurité, les
évolutions technologiques et les normes ou réglementations susceptibles de
s’appliquer.

Il s’agit d’un travail d’analyse et de recommandations : ce dépôt ne constitue
ni une spécification fonctionnelle complète du jeu, ni une implémentation du
service.

## Périmètre de l’équipe

Les travaux couvrent les sujets suivants :

- **Architecture et hébergement** : composants, flux, frontières de confiance,
  dépendances, disponibilité, sauvegardes, reprise après incident et risques
  liés au fournisseur d’hébergement.
- **Sécurité** : menaces, protection des comptes et des données, contrôle
  d’accès, sécurisation des interfaces, journalisation, détection et réponse
  aux incidents.
- **Évolutions technologiques** : changements susceptibles d’affecter le
  service (cloud, conteneurs, IA, nouvelles dépendances ou nouveaux usages),
  risques associés et mesures d’anticipation.
- **Normes et réglementations** : identification des textes et référentiels
  pertinents, analyse de leur applicabilité et recommandations de conformité.

Les fonctionnalités détaillées du jeu, son contenu éditorial et les choix
commerciaux ne sont pas traités, sauf lorsqu’ils influencent directement les
risques ou les obligations du service.

## Organisation documentaire proposée

Le plan détaillé des fichiers, leur objectif et leur contenu attendu sont
décrits dans [`PLAN_DOCUMENTATION.md`](PLAN_DOCUMENTATION.md).

```text
.
├── README.md
├── PLAN_DOCUMENTATION.md
└── docs/
    ├── 01-cadrage/
    ├── 02-architecture-hebergement/
    ├── 03-risques/
    ├── 04-securite/
    ├── 05-evolutions-technologiques/
    └── 06-normes-reglementations/
```

Les dossiers `docs/` sont une structure cible : ils seront créés au fur et à
mesure de la rédaction des livrables.

## Principes de travail

1. Décrire les hypothèses, les actifs, les acteurs et les flux avant d’évaluer
   les risques.
2. Relier chaque risque à ses conséquences, à une mesure de traitement, à un
   responsable et à un risque résiduel.
3. Distinguer les mesures de prévention, de détection, de réaction et de
   continuité.
4. Justifier l’applicabilité des textes et référentiels selon les pays, les
   données, les fonctionnalités et le modèle d’exploitation réellement retenus.
5. Indiquer les sources et la date de vérification des exigences, car les
   normes et réglementations évoluent.

## Applicabilité réglementaire

La liste des textes est à établir et à valider selon le contexte réel du
service. À titre de pistes à examiner, et non de conclusion de conformité :

- RGPD et règles nationales relatives à la protection des données, si des
  données personnelles sont traitées ;
- NIS2 et exigences nationales de cybersécurité, si l’entité et ses activités
  entrent dans leur champ d’application ;
- DSA, si le service relève de ses catégories de services intermédiaires ;
- règles relatives aux jeux d’argent et de hasard, notamment celles applicables
  en France, uniquement si les fonctionnalités constituent une activité de jeu
  réglementée ;
- PCI DSS, si le service stocke, traite ou transmet des données de cartes de
  paiement, ou entre autrement dans le périmètre concerné.

Des référentiels comme ISO/IEC 27001, ISO/IEC 27017, ISO/IEC 27018 et OWASP ASVS
peuvent également servir de repères, sans être automatiquement des obligations
légales. L’analyse devra confirmer les versions applicables et les éventuelles
obligations contractuelles.

## État du projet

Le dépôt contient actuellement le cadrage initial et le plan documentaire.
Les hypothèses métier, l’architecture cible, les juridictions, les catégories
de données et le modèle d’hébergement restent à préciser avant de conclure sur
les risques ou les obligations applicables.