# Système de management - Intégrer la protection des données dans les projets
**Nom du fichier** : 08 - PRO - Intégrer la protection des données dans les projets - TLP RED.md<br>
**Version** du {jj}/{mm}/{aaaa} ({Document de travail | Pour validation | Validé})<br>
**Destinataires** : Parties prenantes du système de management

## Objet du document
Ce document décrit la **procédure à suivre pour intégrer la protection des données (sécurité de l'information et protection de la vie privée) dans les projets**.

Conformément à la section 5.8 de l’annexe A de l’[ISO 27001] et à l’annexe B.8 de l’[ISO 27701] : 
-	elle intègre la protection des données durant tout le cycle de vie des projets, dès leur conception (notion de _security/privacy by design_) et par défaut (notion de _security/privacy by default_) et jusqu’à leur fin de vie ;
-	elle définit les actions à mettre en œuvre dans le cadre des projets pour garantir la protection des données.

Elle s'applique à tous les projets numériques menés dans le périmètre d'application du système de management.

## Informations de versions du document
| <center>**Date**</center> | <center>**Action**</center> | <center>**Auteur**</center> | <center>**État**</center> |
| --- | --- | --- | --- |
| {jj}/{mm}/{aaaa} | {Description de l'action réalisée sur le document} | {Prénom} {NOM} | {Document de travail \| Pour validation \| Validé} |
|  |  |  |  |

<**rôles types à placer dans [Description]** : demandeur, fournisseur de la solution, personne en charge de la protection des données d projet, personne en charge des systèmes informatiques, personne en charge de la sécurité de l'information, personne en charge de la protection de la vie privée><br>
<**docs à référencer dans [Description]** : [Clauses types], [PAS type], [Registre des traitements], références OWASP, ANSSI et CNIL>


## Sommaire

[1. Avant-projet](#1-avant-projet)<br>
&nbsp;&nbsp;&nbsp;&nbsp;[1.1. Faire une proposition : intégrer la protection des données dans la solution proposée](#11-faire-une-proposition--intégrer-la-protection-des-données-dans-la-solution-proposée)<br>

[2. Contractualisation (si besoin)](#2-contractualisation-si-besoin)<br>
&nbsp;&nbsp;&nbsp;&nbsp;[2.1. Contractualiser : vérifier les exigences du demandeur](#21-contractualiser--vérifier-les-exigences-du-demandeur)<br>
&nbsp;&nbsp;&nbsp;&nbsp;[2.2. Alimenter le [Registre des traitements] : remplir les informations obligatoires concernant les traitements sous-traités au fournisseur de la solution](#22-alimenter-le-registre-des-traitements--remplir-les-informations-obligatoires-concernant-les-traitements-sous-traités-au-fournisseur-de-la-solution)<br>

[3. Réalisation du projet](#3-réalisation-du-projet)<br>
&nbsp;&nbsp;&nbsp;&nbsp;[3.1. Cadrer : déterminer les actions à mener pour satisfaire les exigences](#31-cadrer--déterminer-les-actions-à-mener-pour-satisfaire-les-exigences)<br>
&nbsp;&nbsp;&nbsp;&nbsp;[3.2. Piloter : gérer la protection des données dans l’ensemble du projet](#32-piloter--gérer-la-protection-des-données-dans-lensemble-du-projet)<br>
&nbsp;&nbsp;&nbsp;&nbsp;[3.3. Concevoir : protéger les données du projet _by design_](#33-concevoir--protéger-les-données-du-projet-by-design)<br>
&nbsp;&nbsp;&nbsp;&nbsp;[3.4. Développer : intégrer la protection des données dans le développement](#34-développer--intégrer-la-protection-des-données-dans-le-développement)<br>
&nbsp;&nbsp;&nbsp;&nbsp;[3.5. Tester : intégrer la protection des données dans les tests](#35-tester--intégrer-la-protection-des-données-dans-les-tests)<br>
&nbsp;&nbsp;&nbsp;&nbsp;[3.6. Mettre en production : surveiller l’impact, assurer la transmission](#36-mettre-en-production--surveiller-limpact-assurer-la-transmission)<br>
&nbsp;&nbsp;&nbsp;&nbsp;[3.7. Maintenir : garder le système en condition de sécurité](#37-maintenir--garder-le-système-en-condition-de-sécurité)<br>

[4. Finalisation du projet](#4-finalisation-du-projet)<br>
&nbsp;&nbsp;&nbsp;&nbsp;[4.1. Finaliser : restituer, détruire ou autre](#41-finaliser--restituer-détruire-ou-autre)<br>


## 1. Avant-projet

### 1.1. Faire une proposition : intégrer la protection des données dans la solution proposée

1. **Identifier les éléments utiles à la protection des données** (sécurité de l’information et protection de la vie privée) :

    - concernant la **demande** (interne ou externe) :
        - le contexte et le besoin de fond du demandeur ;
        - l’objet du projet : que devons-nous faire/produire ? quelles technologies ? etc.
        - les modalités précises : d’où travaillera-t-on ? sur quel environnement ? via quoi ? etc.

    - concernant la **protection des données** elle-même :
        - les exigences du demandeur en matière de protection des données (dans le cahier des charges, les échanges, etc.) : quel est le niveau d’exigence du demandeur ?

        | <center>**Exigences observées**</center> | <center>**Niveau des exigences**</center> |
        | --- | --- |
        | Aucune exigence des deux parties<br>Note : sauf exception rarissime et dûment justifiée, ce cas ne doit pas exister. | 0. Pas d’exigence |
        | Une exigence générale de sécurité et/ou protection de la vie privée<br>Ex : « assurer la sécurité » | 1. Minimal |
        | Une liste d’exigences classiques | 2. Hygiène |
        | Des exigences nombreuses et/ou spécifiques, mais correspondant à des bonnes pratiques standards | 3. Standard |
        | Des exigences faisant apparaître un besoin de maturité exceptionnel | 4. Renforcé |

        - en matière de sécurité :
            - y a-t-il des besoins spécifiques en termes de disponibilité, intégrité et confidentialité de données ?
            - y a-t-il des indicateurs à produire ?
            - y a-t-il des éléments à journaliser ?
            - quelles sont les modalités souhaitées pour protéger l’accès, le stockage et la transmission de données ?
            - les données fournies seront-elles bien anonymisées ?
        - s’il y a des données à caractère personnel :
            - l’information et l’exercice des droits des personnes concernées sont-ils prévus (droit d’accès à leurs données, modification, etc.) ?
            - la localisation et les durées de conservation des données sont-elles fixées ?
            - un transfert de données en dehors de l’Union européenne est-il prévu ? (autorisation préalable)
            - une sous-traitance ultérieure est-elle prévue ?
        - sur les contraintes : y a-t-il des contraintes à prendre en compte (ex : réglementation à respecter) ? 

2. **Formaliser une proposition qui intègre la protection des données** :
    - expliquer que le fournisseur de la solution gère convenablement sa protection des données internes ;
    - expliquer comment le fournisseur de la solution intègre la protection des données en général, en l’adaptant au contexte :

    | <center>**Niveau des exigences déterminé**</center> | <center>**Explications à fournir**</center> |
    | --- | --- |
    | 0. Pas d’exigences | n.a |
    | 1. Minimal | Le fournisseur de la solution applique les bonnes pratiques en matière de protection des données |
    | 2. Hygiène | Le fournisseur de la solution applique les pratiques définies dans ses [Clauses types] |
    | 3. Standard | Le fournisseur de la solution applique les mesures prévues dans son [PAS type] (au niveau standard) |
    | 4. Renforcé | Le fournisseur de la solution applique les mesures prévues dans son [PAS type] (au niveau renforcé), qui impliquent des coûts supplémentaires |

    - poser les questions auxquelles il faudra absolument répondre (voir points précédents).

## 2. Contractualisation (si besoin)

### 2.1. Contractualiser : vérifier les exigences du demandeur

1. **Valider les exigences du demandeur en matière de protection des données** (dans le projet de contrat et ses annexes, les échanges, etc.) avec l’équipe projet et, si besoin, la personne en charge des systèmes informatiques, la personne en charge de la sécurité de l'information, et la personne en charge de la protection de la vie privée : est-on réellement en mesure de les satisfaire ? doit-on prévoir des surcoûts par rapport aux autres projets ? doit-on ajuster les exigences ? etc.

2. **Fixer le niveau des exigences en matière de protection des données**, en fonction des exigences elles-mêmes (ce niveau peut être ajusté selon la criticité du projet, par exemple), en utilisant le tableau ci-dessous.

3. **Utiliser les éléments types du fournisseur de la solution pour produire/finaliser les documents contractuels en fonction du niveau des exigences** (mais aussi de ce qui est éventuellement imposé dans le contrat), en utilisant le tableau ci-dessous :
    - si aucun document contractuel n’est imposé par le demandeur : les utiliser directement ;
    - si le demandeur impose un document contractuel : vérifier qu’il est bien conforme aux éléments types du fournisseur de la solution et, le cas échéant, les ajuster (contacter la personne en charge de la protection de la vie privée et/ou la personne en charge de la sécurité de l'information et/ou la personne en charge des systèmes informatiques si besoin). 

    | <center>**Niveau des exigences**</center> | <center>**Éléments types du fournisseur de la solution (cumulatifs)**</center> |
    | --- | --- |
    | 1. Minimal | [Clauses types] |
    | 2. Hygiène | [Clauses types] |
    | 3. Standard | [PAS type] (au niveau standard) |
    | 4. Renforcé | [PAS type] (au niveau renforcé) |

### 2.2. Alimenter le [Registre des traitements] : remplir les informations obligatoires concernant les traitements sous-traités au fournisseur de la solution

1. **Remplir les champs nécessaires au [Registre des traitements]** (avec l’aide de la personne en charge de la protection de la vie privée si nécessaire).

## 3. Réalisation du projet

### 3.1. Cadrer : déterminer les actions à mener pour satisfaire les exigences

D’une manière générale, cette phase est l’occasion de faire le point sur les exigences en matière de protection des données et sur ce qu’on s’est engagé à mettre en place, ainsi que d’obtenir des réponses à nos questions et fournir des réponses aux questions du demandeur.

1. **Valider la gouvernance** (cf. [PAS type]).

2. **Concrétiser/traduire les exigences** relatives à la protection des données, quel que soit leur niveau, en actions concrètes (si besoin).

3. **Attribuer les exigences et/ou actions** (personne en charge de la protection des données du projet, fournisseur de la solution, personne en charge des systèmes informatiques, demandeur, etc.).

### 3.2. Piloter : gérer la protection des données dans l’ensemble du projet

1. **Désigner la personne en charge de la protection des données du projet** (par défaut, il s’agit du chef de projet du fournisseur de la solution, qui peut déléguer cette fonction), et le faire connaître au demandeur.

2. **Assurer un suivi des actions relatives à la protection des données et tenir le demandeur informé** (ex : lors de "comités de pilotage") : 
    - garantir que les bonnes pratiques en matière de protection des données sont mises en œuvre (développement sécurisé, respect de la règlementation, etc.) ;
    - garantir que les exigences seront satisfaites ;
    - garantir que les actions concrètes seront appliquées ;
    - garantir que les instructions du responsable du traitement sont respectées ;
    - garantir l’obtention de l’autorisation préalable écrite du responsable du traitement en cas de transfert en dehors de l’Union européenne ou en cas de sous-traitance ultérieure (et le cas échéant, garantir la conclusion d’un contrat avec le sous-traitant ultérieur).

3. **Jouer un rôle d’interface et assister le demandeur en matière de protection des données**, pour prendre ses demandes et questions en compte et, le cas échéant, transmettre toute information requise par les exigences (incidents de sécurité, violations de données, réclamations de personnes concernées, etc.).

Note : la personne en charge de la protection des données peut faire appel à la personne en charge de la sécurité de l'information et à la personne en charge de la protection de la vie privée en cas de besoin.

### 3.3. Concevoir : protéger les données du projet _by design_

Note : ces actions précisent ou illustrent les exigences types liées aux projets.

1. **Déterminer les bonnes pratiques applicables** :
    - lister les supports (matériels, logiciels, réseaux, etc.) / technologies, ex : langage de développement, _framework_ de développement, plateformes _cloud_ ;
    - identifier les bonnes pratiques (internes ou externes) par support / technologie (principe de moindre privilège, protocoles sécurisés, réduction de la surface d'attaque du produit, usage de format standard, réduction des vulnérabilités résiduelles classiques, etc.) :
        - référentiels internes ;
        - référentiels externes (ex : ANSSI, OWASP, CNIL) ;
        - solutions labelisées par l’ANSSI ou équivalent. 

### 3.4. Développer : intégrer la protection des données dans le développement

1. **Mettre en œuvre les actions et/ou mesures prévues** lors de la phase de conception.

2. **Appliquer les bonnes pratiques de développement** (_DevSecOps_), ex :
    - paramétrage des environnements d'exécution et de compilation ;
    - pratiques et méthodologies pour le développement sécurisé (déploiement des correctifs de sécurité, intégration et usage correct des moyens cryptographiques et des mots de passe, configurations protectrices par défaut, etc.) :
        - _[Security Knowledge Framework](https://www.securityknowledgeframework.org/)_ ;
        - _[Secure your application](https://docs.gitlab.com/ee/user/application_security/)_ (GitLab) ;
        - _[Securing your development environment](https://stsewd.dev/posts/securing-your-dev-environment/)_ (Santos Gallegos) ;
        - [Guide RGPD du développeur](https://lincnil.github.io/Guide-RGPD-du-developpeur/) (ex : _privacy by design_ et _by default_) ;
    - « signature » de code (non-répudiation).

3. **Documenter les fonctionnalités relatives à la protection des données**, au même titre que les autres fonctionnalités du produit.

### 3.5. Tester : intégrer la protection des données dans les tests

1. **Tester l’objet du projet** selon le niveau des exigences :

    | <center>**Niveau des exigences**</center> | <center>**Tests à réaliser (cumulables)**</center> |
    | --- | --- |
	| 1. Minimal | Tests des fonctionnalités liées à la protection des données |
    | 2. Hygiène | Validation de la sécurité (vérification de la présence de vulnérabilités) :<br>- Recherche / scans de vulnérabilités (ex : wpscan, nmap-vulscan)<br>- Tests de sécurité automatiques (ex : SonarQube) |
    | 3. Standard | Revue de code par des pairs<br>Tests spécifiques :<br>- Tests de sécurité web (ex : _[OWASP Web Security Testing Guide](https://owasp.org/www-project-web-security-testing-guide/)_)<br>- Tests de sécurité mobile (ex : _[OWASP Mobile Security Testing Guide](https://owasp.org/www-project-mobile-security-testing-guide/)_) |
    | 4. Renforcé | Audits de sécurité (de code, d’architecture et de configuration)<br>Tests d’intrusion |

2. **Corriger les vulnérabilités** détectées :
    - celles détectées par les tests ;
    - celles détectées par les vérifications du demandeur.

### 3.6. Mettre en production : surveiller l’impact, assurer la transmission

1. **Porter une attention particulière aux potentiels effets de bord** consécutifs à la mise en production (ex : incompatibilités, ouvertures de flux non prévus, etc.).

2. Lors de la phase de déploiement, il convient de former et d'**assurer la prise en compte du changement** auprès des administrateurs / exploitants en fonction du niveau des exigences et en s'appuyant sur les bonnes pratiques. 

### 3.7. Maintenir : garder le système en condition de sécurité

1. **Respecter les exigences / appliquer les mesures**, notamment en matière de :
    - veille sur les composants du projet et leurs vulnérabilités ;
    - application des mises à jour et correctifs de sécurité ;
    - gestion des changements et de l’obsolescence des composants des systèmes : s’assurer que la sécurité ne se dégrade pas ;
    - surveillance des systèmes : gestion des alertes et des journaux d’événements ;
    - gestion des incidents : qualification (niveau, présence de données à caractère personnel, etc.), escalade, notifications.

## 4. Finalisation du projet

### 4.1. Finaliser : restituer, détruire ou autre

1. **Respecter les exigences / appliquer les mesures**, notamment en matière de :
    - restitution / libération des ressources (code, environnement, accès, équipements, etc.) ;
    - archivage des données ;
    - effacement sécurisé.

2. **Vérifier les possibilités de capitaliser sur le projet** (ex : rédaction d'un guide interne, réalisation d'un retour d’expérience, etc.).
