# ✦ GitOsint

<p align="center">
  <img src="https://img.shields.io/badge/HTML-FF7A00?style=for-the-badge&logo=html5&logoColor=white" />
  <img src="https://img.shields.io/badge/CSS-1572B6?style=for-the-badge&logo=css3&logoColor=white" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=000" />
</p>

<p align="center">
  <b>GitOsint</b> est une interface web OSINT minimaliste pour explorer un profil GitHub public, analyser ses dépôts et récupérer les e-mails visibles dans les commits.
</p>

---

## ✨ Ce que fait le projet

- 🔎 recherche un utilisateur GitHub par pseudo ;
- 👤 affiche les infos publiques du profil ;
- 📦 scanne les dépôts publics non fork ;
- 🧾 analyse les commits publics ;
- ✉️ détecte les e-mails trouvés ;
- 📤 exporte les résultats en `CSV` ou `JSON` ;
- 🔐 accepte un token GitHub facultatif pour éviter les limites d’API.

---

## 🖼️ Interface

Le projet utilise un design sombre, avec :
- un fond animé ;
- un style glassmorphism ;
- des inputs fins et modernes ;
- une carte de résultats compacte ;
- une barre de progression élégante ;
- des boutons d’export propres.

---

## 🚀 Utilisation

1. Ouvre `gitosint.html` dans ton navigateur.
2. Entre un pseudo GitHub.
3. Ajoute un token si besoin.
4. Clique sur **Scan**.
5. Consulte les infos du profil, les dépôts scannés et les e-mails extraits.
6. Exporte les données au format `CSV` ou `JSON`.

Exemple :
```txt
Pseudo : torvalds
Token : optionnel
```

---

## 🧠 Données affichées

### Profil
- ID ;
- login ;
- nom ;
- bio ;
- type de compte ;
- site admin ;
- hireable ;
- e-mail ;
- localisation ;
- entreprise ;
- site web ;
- Twitter ;
- URL GitHub ;
- stats publiques ;
- date de création ;
- date de mise à jour.

### Scan
- nombre de dépôts scannés ;
- nombre de commits scannés ;
- nombre d’e-mails trouvés ;
- source de chaque e-mail.

---

## 📁 Fichier principal

```txt
gitosint.html
```

Tout le projet est contenu dans un seul fichier HTML :
- structure ;
- styles ;
- logique JavaScript ;
- export des données.

---

## ⚙️ Token GitHub

Le token est **optionnel**, mais conseillé si tu veux limiter les erreurs de rate limit.

Format attendu :
```txt
ghp_xxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

---

## 📦 Exports

### CSV
Le CSV contient :
- les métadonnées du scan ;
- les infos du compte ;
- la liste des e-mails détectés ;
- la source associée.

### JSON
Le JSON contient :
- les métadonnées ;
- les données du profil ;
- la liste complète des e-mails ;
- les dates de première apparition.

---

## ⚠️ Limites

- seules les données publiques sont accessibles ;
- certains profils n’ont pas d’e-mail visible ;
- sans token, l’API GitHub peut limiter les requêtes ;
- les repos fork ne sont pas scannés.

---

## 🛡️ Usage responsable

GitOsint doit être utilisé uniquement sur des données publiques et dans un cadre légal.  
Il est destiné à l’exploration technique, pas à l’exploitation abusive de données personnelles.

---

## 🔧 Améliorations possibles

- ajout d’un loader plus visuel ;
- pagination des résultats ;
- filtres par source d’e-mail ;
- historique des scans ;
- séparation HTML / CSS / JS ;
- dark mode encore plus poussé ;
- mini prévisualisation du profil scanné.

---

## 💬 À propos

Projet léger, rapide et centré sur une interface propre pour l’OSINT GitHub.

---

## 🎯 Nom du fichier

Le fichier principal est :
```txt
gitosint.html
```
