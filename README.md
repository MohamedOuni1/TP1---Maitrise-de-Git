<h2 style="color: red; text-decoration: underline;">Partie 1 : Préparation de l'environnement Git</h2>
## Partie 1 : Préparation de l'environnement Git
### 4. Comment vérifier la configuration actuelle de Git sur votre machine, notamment le nom d’utilisateur et l’adresse e-mail ?

```bash
git config --global user.email
```
## 5. Comment modifier votre adresse e-mail si vous l'avez mal configurée lors de l'installation de Git ?

```bash
git config --global user.email "votre.email@example.com"
git config user.email "votrenouveauemail@example.com"
```
## Partie 2: Création d'un nouveau projet
### 6. Si vous avez oublié de créer un fichier README.md lors de l'initialisation du projet, comment pouvez-vous l'ajouter après coup et commiter les changements ?

```bash
touch README.md
nano README.md  
git add README.md
git commit -m "Ajout du fichier README.md"
git push origin main
```

### 7. Comment définir un dépôt distant si vous n'en avez pas configuré un lors de la création du projet ?
```bash
git remote add origin <URL-du-dépôt>
git remote set-url origin <URL-du-dépôt>
git remote -v
```

# Partie 3 : Concepts de base de Git
### 3. Comment annuler les modifica�ons locales d'un fichier avant de les ajouter à l'index ?
```bash
git checkout -- nom_du_fichier
```
### 4. Comment visualiser les fichiers qui sont prêts à être commités dans Git (staging) ?
```bash
git status
```

# Partie 4 : Collaborer sur Git
### 4. Comment suivre (track) un dépôt distant et récupérer toutes les branches de ce dépôt ?
```bash
git remote add origin <URL-du-dépôt>
git fetch origin
git branch -a
git checkout -b nom_de_votre_branche origin/nom_de_la_branche_distant
```

### 5. Comment supprimer une branche locale après l'avoir fusionnée dans master ?
```bash
git branch -d nom_de_la_branche
git branch -D nom_de_la_branche
```

# Partie 5 : Rebase d'une branche sur ‘master’

### 8. Comment interrompre un rebase en cours si vous avez commis une erreur ?
```bash
git rebase --abort
```
### 9. Comment lister les commits qui vont être rebasés avant de lancer un rebase ?
```bash
git log --oneline <branche_cible>..<branche_source>
```

# Partie 6 : Utilisation de Gitlow

### 8. Comment afficher la liste des branches ac�ves et en cours de développement dans Gitlow ?
```bash
git flow feature list
```
### 9. Comment annuler une branche de correctif (hotix) avant de la finaliser si vous constatez une erreur ?
```bash
git flow hotfix abort
```
