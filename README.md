# TP Symfony - Environnement PHP 7.4

Ce projet est un **starter Symfony vierge** configuré pour fonctionner en **PHP 7.4**.  
Il est distribué via **GitHub Classroom** : chaque étudiant a son dépôt personnel.

---

## 🚀 Étapes pour démarrer

### 1. Ouvrir le projet
- Cliquez sur le bouton **“Open in Codespaces”** dans GitHub.  
- Attendez quelques minutes : l’environnement PHP 7.4 + Composer sera automatiquement configuré.  
- Les dépendances Symfony seront installées (`composer install` est exécuté automatiquement).

---

### 2. Configurer la base de données
⚠️ Vous **n’avez pas de MySQL local** dans Codespaces : la base de données est hébergée sur le serveur du BTS.  

- Créez un fichier `.env.local` à la racine du projet.  
- Ajoutez la ligne suivante en adaptant les valeurs (`user`, `password`, `dbname`, `host` fournis par le professeur) :

```dotenv
DATABASE_URL="mysql://user:password@serveur.externe:3306/nom_de_la_base"
