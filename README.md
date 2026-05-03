# GitOsint

<p align="center">
  <img src="https://img.shields.io/badge/HTML-CSS-JS-111111?style=for-the-badge&logo=html5&logoColor=white" alt="Tech Stack">
  <img src="https://img.shields.io/badge/License-MIT-111111?style=for-the-badge" alt="License">
  <img src="https://img.shields.io/badge/OSINT-GitHub-111111?style=for-the-badge" alt="OSINT">
</p>

<p align="center">
  <b>GitOsint</b> est une interface web OSINT élégante pour analyser un utilisateur GitHub à partir de données publiques.
</p>

---

## Présentation

GitOsint permet de rechercher un pseudo GitHub, d’afficher les informations publiques du profil, d’explorer les dépôts et les commits publics, puis d’extraire les adresses e-mail visibles dans les métadonnées GitHub.

L’interface a été pensée pour être :
- sombre et minimaliste ;
- rapide à utiliser ;
- orientée lecture et export ;
- simple à héberger comme une page HTML statique.

---

## Fonctionnalités

- Recherche d’un utilisateur GitHub par pseudo.
- Affichage du profil public.
- Scan des dépôts publics non fork.
- Analyse des commits publics.
- Extraction des e-mails détectés.
- Export des résultats en `CSV` et `JSON`.
- Copie rapide de certaines valeurs.
- Ajout facultatif d’un token GitHub pour réduire les limites API.

---

## Aperçu

L’interface comprend :
- un champ de recherche principal ;
- un champ token repliable ;
- une carte de résultats animée ;
- une barre de progression ;
- un export des données à la fin du scan.

---

## Installation

### 1. Récupérer le projet
```bash
git clone https://github.com/ton-utilisateur/GitOsint.git
cd GitOsint
```

### 2. Ouvrir l’application
Ouvre simplement le fichier `index.html` dans un navigateur moderne.

### 3. Lancer un scan
- saisis un pseudo GitHub ;
- ajoute un token si nécessaire ;
- clique sur **Scan**.

---

## Utilisation

1. Entre un nom d’utilisateur GitHub.
2. Clique sur **Scan**.
3. Consulte le profil, les stats et les e-mails trouvés.
4. Exporte les résultats en `CSV` ou `JSON`.

Exemple d’usage :
- pseudo : `torvalds`
- token : optionnel
- export : `gitosint_torvalds.csv`

---

## Export des données

### CSV
Le fichier CSV contient :
- les métadonnées du scan ;
- les informations principales du profil ;
- la liste des e-mails détectés ;
- la source associée à chaque e-mail.

### JSON
Le fichier JSON contient :
- les métadonnées ;
- l’objet complet du compte ciblé ;
- les e-mails trouvés avec leur source et leur date de première apparition.

---

## Configuration du token

Le token GitHub est optionnel, mais recommandé pour éviter les limites de rate limit.

Format attendu :
```txt
ghp_xxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

---

## Limites

- L’outil n’analyse que les données publiques.
- Certains profils n’ont aucun e-mail visible.
- Les résultats dépendent de ce que l’API GitHub renvoie.
- Sans token, les requêtes peuvent être limitées.

---

## Sécurité

GitOsint doit être utilisé de manière légale, éthique et responsable.  
Il ne doit servir qu’à analyser des données publiques et accessibles sans autorisation spéciale.

---

## Structure du projet

```txt
index.html
README.md
```

---

## Roadmap

- amélioration du design responsive ;
- ajout d’un historique de scans ;
- filtrage des e-mails par source ;
- meilleure gestion des erreurs API ;
- séparation du CSS et du JavaScript ;
- support de plusieurs profils à la suite.

---

## Licence

À définir selon ton usage.

---

## Crédits

Développé pour l’analyse OSINT de profils GitHub à partir de données publiques.
