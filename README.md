# GitOsint

GitOsint est une interface web d’OSINT pour GitHub permettant de rechercher un utilisateur, d’analyser son profil public, de parcourir ses dépôts et ses commits publics, puis d’extraire les adresses e-mail visibles dans les données publiques GitHub.

## Aperçu

L’application propose une interface sombre, minimaliste et animée, avec :
- recherche d’un nom d’utilisateur GitHub ;
- ajout optionnel d’un token GitHub pour éviter les limites de rate limit ;
- affichage du profil GitHub ;
- scan des dépôts publics et des commits associés ;
- extraction des e-mails trouvés ;
- export des résultats en CSV ou JSON.

## Fonctionnalités

- Recherche d’un compte GitHub par pseudo.
- Affichage des informations publiques du profil :
  - identifiant,
  - nom,
  - bio,
  - type de compte,
  - e-mail,
  - localisation,
  - société,
  - site web,
  - compte Twitter,
  - statistiques publiques.
- Scan des dépôts publics non fork.
- Analyse des commits publics.
- Détection et suppression des e-mails de type `noreply`.
- Export des résultats en :
  - `CSV`,
  - `JSON`.
- Boutons de copie rapides pour certaines valeurs.

## Démo

Le projet fonctionne comme une page HTML autonome.  
Il suffit d’ouvrir le fichier dans un navigateur moderne et de saisir un pseudo GitHub.

## Prérequis

- Un navigateur web moderne.
- Une connexion Internet.
- Un token GitHub optionnel pour améliorer les limites d’API.

## Installation

1. Clone ce dépôt :
```bash
git clone https://github.com/ton-utilisateur/gitosint.git
```

2. Ouvre le fichier `index.html` dans ton navigateur.

3. Renseigne un pseudo GitHub dans le champ de recherche.

4. Lance le scan.

## Utilisation

1. Entre un nom d’utilisateur GitHub.
2. Ajoute un token si nécessaire.
3. Clique sur **Scan**.
4. Consulte :
   - les données du profil,
   - les statistiques de scan,
   - les e-mails trouvés.
5. Exporte les résultats au format CSV ou JSON.

## Token GitHub

L’ajout d’un token est facultatif, mais recommandé pour réduire les erreurs liées aux limites de l’API GitHub.

Format attendu :
```txt
ghp_XXXXXXXXXXXXXXXXXXXXXXXXXXXX
```

## Structure des données

Le scan récupère :
- les données du profil GitHub via l’API utilisateurs ;
- les dépôts publics via l’API repos ;
- les commits publics liés aux dépôts ;
- les événements publics si nécessaire.

Les résultats exportés contiennent :
- les informations générales du profil ;
- les statistiques du scan ;
- la liste des e-mails détectés ;
- la source associée à chaque e-mail.

## Export

### CSV
Le fichier CSV contient :
- les métadonnées du scan ;
- les informations du profil ;
- les e-mails trouvés triés par ordre alphabétique ;
- la source et l’horodatage de la première apparition.

### JSON
Le fichier JSON contient :
- les métadonnées du scan ;
- l’objet `target` avec les infos du compte ;
- la liste complète des e-mails détectés.

## Limites

- GitHub ne renvoie que les données publiques.
- Certains profils n’ont pas d’e-mail public.
- Les scans peuvent être limités par l’API GitHub sans token.
- Les commits ou événements privés ne sont pas accessibles.

## Sécurité et usage responsable

GitOsint doit être utilisé uniquement sur des données publiques et dans un cadre légal et éthique.  
Ne l’utilise pas pour collecter, stocker ou diffuser des données personnelles sans autorisation.

## Développement

Le projet est une page HTML/CSS/JavaScript autonome.  
Pour le modifier, il suffit d’éditer le fichier HTML principal.

### Fichiers principaux
- `index.html` : interface, styles et logique JavaScript.

## Améliorations possibles

- ajout d’un système de recherche plus avancé ;
- filtrage des résultats ;
- pagination des e-mails ;
- meilleure gestion des erreurs API ;
- historique des scans ;
- support multi-profils.
