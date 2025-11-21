# Système de management - Gérer les risques
**Nom du fichier** : 06 - PRO - Gérer les risques - TLP AMBER.md<br>
**Version** du {jj}/{mm}/{aaaa} ({Document de travail | Pour validation | Validé})<br>
**Destinataires** : Parties prenantes du système de management

## [Avant-propos]

Ce document a été créé pour un système de management de la protection des données (sécurité de l'information ET protection de la vie privée) d'une petite organisation.

Les principaux **contributeurs** sont les suivants :
- Matthieu GRALL.

Les **versions** du document sont les suivantes :
| <center>Version</center> | <center>Action</center> | <center>Éditeur</center> |
| --- | --- | --- |
| 01/11/2025 (v0.1) | Création du document | Matthieu GRALL |
| 21/11/2025 (v0.2) | Ajout de l'avant-propos et corrections mineures | Matthieu GRALL |

Il est placé sous la **licence** suivante :
_[Creative Commons Attribution 4.0 International License][cc-by]_.

[![CC BY 4.0][cc-by-image]][cc-by]

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg

## Objet du document

Ce document décrit la **méthode de gestion des risques liés à la protection des données (sécurité de l'information et protection de la vie privée) qui pèsent sur l'organisation et sur les personnes concernées**.

Conformément à la section 6.1 de l’[ISO/IEC 27001] :
-	il présente la démarche permettant d’apprécier les risques ;
-	il décrit comment traiter les risques ;
-	il explique les modalités d’amélioration continue.

C'est une application d’[EBIOS _Risk Manager_] au contexte spécifique du système de management. Elle est compatible avec les normes [ISO 31000] et [ISO/IEC 27005].

Il s'applique à tous les projets numériques menés dans le périmètre d'application du système de management.

## Informations de versions du document

| <center>**Date**</center> | <center>**Action**</center> | <center>**Auteur**</center> | <center>**État**</center> |
| --- | --- | --- | --- |
| {jj}/{mm}/{aaaa} | {Description de l'action réalisée sur le document} | {Prénom} {NOM} | {Document de travail \| Pour validation \| Validé} |
|  |  |  |  |

## Sommaire

[1. Évaluer la conformité au socle de règles](#1-évaluer-la-conformité-au-socle-de-règles)<br>
[2. Apprécier les risques](#2-apprécier-les-risques)<br>
[3. Évaluer les risques](#3-évaluer-les-risques)<br>
[4. Traiter les risques](#4-traiter-les-risques)<br>
[5. Accepter les risques](#5-accepter-les-risques)<br>
[6. Surveiller et revoir les risques](#6-surveiller-et-revoir-les-risques)<br>
[7. Communiquer sur les risques](#7-communiquer-sur-les-risques)<br>

## Procédure : l'application d'[EBIOS _Risk Manager_] à l'organisation

Note : la présente procédure est faite de telle sorte que les itérations successives de l’étude des risques produisent des résultats cohérents, valides et comparables.

### 1. Évaluer la conformité au socle de règles

Note : ce sous-processus fait partie du traitement des risques de l’[ISO/IEC 27005] et de l’atelier 1 d’[EBIOS _Risk Manager_].

Dans le contexte de l'organisation où le socle de règles est constitué par sa [Politique générale], la démarche est la suivante :
1. évaluer la **pertinence des règles**, dans la [Déclaration d’applicabilité], au regard :
    1. des bonnes pratiques de sécurité de l’information et de protection de la vie privée ;
    2. des évolutions du contexte de l'organisation ;
    3. des difficultés d’application identifiées (ex : au regard des demandes de dérogation) ;
2. évaluer la **conformité aux règles** sur la base du contrôle interne ;
3. évaluer l’**avancement des actions** destinées à traiter des risques dans le [Suivi des actions].

### 2. Apprécier les risques

#### Apprécier les événements redoutés

Note : ce sous-processus fait partie des processus d’établissement du contexte et d’appréciation des risques de l’[ISO/IEC 27005] et de l’atelier 1 d’[EBIOS _Risk Manager_].

Dans le contexte de l'organisation, les conséquences potentielles des risques portent :
- non seulement sur l’organisme (sécurité de l’information) ;
- mais aussi sur les personnes concernées (protection de la vie privée).

La démarche est la suivante, compte tenu du socle de règles et des mesures existantes ou prévues :
1. identifier les **valeurs métier** (ce qu’on veut protéger : les processus de l'organisation et les données afférentes) et leurs propriétaires sur la base du domaine d’application du système de management ;
2. pour chaque valeur métier, déterminer les **conséquences potentielles (sur l'organisation et sur les personnes concernées)** en utilisant l’annexe « Échelle de gravité » en cas de :
    1. accès non autorisé à des données ;
    2. modification non désirée de données ;
    3. disparition de données ;
3. estimer la **gravité** de ces événements redoutés en utilisant l’annexe  « Échelle de gravité » : la gravité d’un événement redouté est égale à la gravité la plus haute de tous les conséquences potentielles).

#### Apprécier les sources de risques

Note : ce sous-processus fait partie du processus d’appréciation des risques de l’[ISO/IEC 27005] et de l’atelier 2 d’[EBIOS _Risk Manager_].

La démarche est la suivante, compte tenu du socle de règles et des mesures existantes ou prévues :
1. pour chaque événement redouté, identifier la **source de risques** la plus pertinente et son **objectif visé**.

#### Apprécier les scénarios stratégiques

Note : ce sous-processus fait partie du processus d’appréciation des risques de l’[ISO/IEC 27005] et de l’atelier 3 d’[EBIOS _Risk Manager_].

La démarche est la suivante, compte tenu du socle de règles et des mesures existantes ou prévues :
1. pour chaque événement redouté, déterminer le **scénario stratégique** (chemin dans l’écosystème que les sources de risques pourraient emprunter pour atteindre leur objectif visé) le plus vraisemblable.

#### Apprécier les scénarios opérationnels

Note : ce sous-processus fait partie des processus d’établissement du contexte et d’appréciation des risques de l’[ISO/IEC 27005] et des ateliers 1 et 4 d’[EBIOS _Risk Manager_].

La démarche est la suivante, compte tenu du socle de règles et des mesures existantes ou prévues :
1. déterminer les **scénarios opérationnels** (séquences d’actions qui pourraient permettre leur réalisation) et sélectionner le plus vraisemblable ;
2. identifier les principaux **biens supports** (systèmes, personnes et locaux sur lesquels reposent les valeurs métier considérées, et dont les vulnérabilités seraient exploitées) et leurs propriétaires ;
3. estimer la **vraisemblance** des scénarios opérationnels ainsi obtenus en utilisant l’annexe « Échelle de vraisemblance ».

### 3. Évaluer les risques

Note : ce sous-processus fait partie du processus d’évaluation des risques de l’[ISO/IEC 27005] et de l’atelier 5 d’[EBIOS _Risk Manager_].

La démarche est la suivante, compte tenu du socle de règles et des mesures existantes ou prévues :
1. déterminer les **propriétaires des risques** : pour chaque risque, son propriétaire est le propriétaire de la valeur métier concernée ;
2. **évaluer les risques** en utilisant l’annexe « Matrice de détermination du niveau des risques » ;

### 4. Traiter les risques

Note : ce sous-processus fait partie du processus de traitement des risques de l’[ISO/IEC 27005] et de l’atelier 5 d’[EBIOS _Risk Manager_].

La démarche est la suivante :
1. déterminer les **options de traitement** privilégiées en utilisant l’annexe « Matrice de détermination du niveau des risques » ;
2. déterminer les **mesures**, conformément aux options privilégiées, pour :
    1. le cas échéant, compléter la conformité au socle ;
    2. le cas échéant, agir sur ces événements redoutés ;
    3. le cas échéant, agir sur les sources de risques ;
    4. le cas échéant, agir sur ces scénarios stratégiques ;
    5. agir sur les scénarios opérationnels ;
3. vérifier la **complétude** et la **cohérence des mesures** ;
4. le cas échéant, mettre la **[Déclaration d’applicabilité]** à jour si certains des risques appréciés justifient particulièrement des mesures de celle-ci ;
5. estimer la **gravité et** la **vraisemblance des risques résiduels** en utilisant les annexes « Échelle de gravité » et « Échelle de vraisemblance ».

### 5. Accepter les risques

Note : ce sous-processus fait partie du processus d’acceptation des risques de l’[ISO/IEC 27005] et de l’atelier 5 d’[EBIOS _Risk Manager_].

La démarche est la suivante :
1. **les risques appréciés sont approuvés** par leurs propriétaires au regard de l’étude réalisée ;
2. **les risques résiduels sont approuvés** par leurs propriétaires en utilisant l’annexe « Matrice de détermination du niveau des risques » ;
3. **les mesures inscrites au [Suivi des actions] sont approuvées** par les responsables de leur mise en œuvre.

### 6. Surveiller et revoir les risques

Note : ce sous-processus fait partie du processus de surveillance et revue des risques de l’[ISO/IEC 27005] et de l’ensemble d’[EBIOS _Risk Manager_].

La démarche est la suivante :
1. **les risques de niveau 2** (cf. annexe « Matrice de détermination du niveau des risques ») **font l’objet d’une surveillance** (orientation du programme annuel de contrôle interne, et éventuellement indicateurs) ;
2. **la mise en œuvre des mesures est suivie** à l’aide du [Suivi des actions] ;
3. **l’étude des risques est revue**, en vérifiant que l’ensemble de son contenu est toujours pertinent et ne doit pas intégrer de nouveaux paramètres, et le cas échéant en la mettant à jour de manière cohérente, au moins une fois par an, et dans les cas suivants :
    1. un changement significatif dans les principaux composants de l’étude :
        1. des règles structurantes ;
        2. des valeurs métier ;
        3. des biens supports importants ;
        4. des parties prenantes ;
    2. la survenance d’un incident grave.

### 7. Communiquer sur les risques

Note : ce sous-processus fait partie du processus de communication relative aux risques de l’[ISO/IEC 27005] et de l’ensemble d’[EBIOS _Risk Manager_].

La démarche est la suivante :
1. l’étude des risques fait l’objet d’un **travail collaboratif** impliquant la participation active de nombreux acteurs selon les sous-processus : la direction, les opérationnels, la personne en charge du système de management et les expertises nécessaires ;
2. les principaux risques sont utilisés pour **sensibiliser** les collaborateurs.

## Annexe

### Échelle de gravité

Le tableau suivant présente l’échelle utilisée pour estimer la gravité des risques :

| <center>Gravité</center> | <center>Conséquences financières</center> | <center>Conséquences opérationnelles</center> | <center>Conséquences sur l'image</center> | <center>Conséquences juridiques</center> | <center>Conséquences sur la vie privée</center> |
| --- | --- | --- | --- | --- | --- |
| 1. Minimale | Aucun ou seulement quelques dizaines ou centaines d’euros annuels | Aucun ou seulement dégradation fonctionnelle avec peu de conséquence sur un processus | Aucun ou conséquence négligeable sur l’image | Aucun ou seulement sanction interne | Aucun ou seulement désagrément matériel, moral ou physique négligeable (ex : _spam_) |
| 2. Limitée | Milliers d’euros annuels | Dégradation fonctionnelle limité sur un processus | Image impactée, mais de manière circonscrite et temporaire | Pénalités contractuelles avec des petits clients | Désagrément matériel, moral ou physique significatif, qui pourra être surmonté après quelques difficultés |
| 3. Importante | Une dizaine de milliers d’euros annuels | Dégradation fonctionnelle limitée sur plusieurs processus | Image atteinte de manière publique, mais limitée dans le temps | Pénalités contractuelles fortes (avec des grands comptes), mention dans une affaire civile ou pénale, non-respect de la loi et de la réglementation (protection de la vie privée notamment), enquête administrative, condamnation ou amende | Conséquence matérielle, morale ou physique qui ne sera surmontée qu’avec difficultés |
| 4. Maximale | Plus qu’une dizaine de milliers d'euros annuels | Arrêt fonctionnel sur l’ensemble des processus | Image dégradée de manière profonde et durable | Non-respect majeur de la loi et de la réglementation (protection de la vie privée notamment), condamnation pénale, pénalités contractuelles avec plusieurs acteurs | Conséquence matérielle, morale ou physique qui pourrait ne pas être surmontée.
 
### Échelle de vraisemblance

Le tableau suivant présente l’échelle utilisée pour estimer la vraisemblance des risques :

| Vraisemblance | Description |
| --- | --- |
| 1. Minimale | La source de risque a peu ou pas de chances d’atteindre son objectif et ce, peu importe les scénarios opérationnels envisagés. |
| 2. Limitée | Le contexte peut apporter à la source de risque les ressources nécessaires pour atteindre son objectif selon certains modes opératoires prouvés comme étant possibles (_zero day_, compromission, etc.). |
| 3. Importante | La source de risque possède les ressources nécessaires pour atteindre son objectif selon certains modes opératoires prouvés comme étant possibles. |
| 4. Maximale | Un tel scénario s’est déjà produit au sein de l'organisation ou d’autres entreprises analogues. |

### Matrice de détermination du niveau des risques

Le schéma suivant présente la matrice utilisée pour déterminer le niveau de risque :

| <center>Niveau de risque</center> |  | <center>**Vraisemblance**</center> |  | |  |
| --- | --- | --- | --- | --- | --- |
|  | | 1. Minimale | 2. Limitée | 3. Importante | 4. Maximale |
| **Gravité** | 4. Maximale | **3. Important** | **3. Important** | **4. Maximal** | **4. Maximal** |
|  | 3. Importante | **3. Important** | **3. Important** | **4. Maximal** | **4. Maximal** |
|  | 2. Limitée | **1. Minimal** | **1. Minimal** | **2. Limité** | **2. Limité** |
|  | 1. Minimale | **1. Minimal** | **1. Minimal** | **2. Limité** | **2. Limité** |

Le tableau suivant présente les options de traitement privilégiées en fonction du niveau de risque :

| <center>Niveau de risque</center> | <center>Description</center> | <center>Options de traitement privilégiées</center> |
| --- | --- | --- |
| 1. Minimal | Acceptables | Pas besoin de mesures additionnelles |
| 2. Limité | Incidents | Surveiller |
| 3. Important | Sinistres | transférer (si possible) ou réduire |
|4. Maximal | Inacceptables | Traiter absolument (toutes options possibles) |
