
# 🚀 Mon Projet Symfony 7.2

Bienvenue dans **Mon Projet Symfony 7.2** ! Ce projet est basé sur la version 7.2 du framework PHP Symfony. Il fournit une base solide pour le développement d'applications web modernes et performantes.

## 📖 Table des matières

- [🛠 Prérequis](#-prérequis)
- [📦 Installation](#-installation)
- [🚀 Lancement](#-lancement)
- [📂 Structure du projet](#-structure-du-projet)
- [⚙️ Configuration](#-configuration)
- [📜 Licence](#-licence)

---

## 🛠 Prérequis

Avant de commencer, assurez-vous d'avoir les prérequis suivants installés :

- **PHP 8.2** ou supérieur
- **Composer** (gestionnaire de dépendances PHP)
- **Symfony CLI** (optionnel, mais recommandé)
- **Une base de données** (MySQL, PostgreSQL, SQLite, etc.)
- **Node.js & npm** (si vous utilisez Webpack Encore pour les assets)

## 📦 Installation

Clonez ce dépôt et installez les dépendances :

```sh
git clone https://github.com/utilisateur/mon-projet-symfony.git
cd mon-projet-symfony
composer install
```

Si votre projet utilise un fichier `.env`, créez une copie de l'exemple :

```sh
cp .env.example .env
```

Puis, générez votre clé secrète et mettez à jour votre base de données :

```sh
php bin/console doctrine:database:create
php bin/console doctrine:migrations:migrate
```

## 🚀 Lancement

Démarrez le serveur Symfony :

```sh
symfony server:start
```

Ou avec le serveur interne de PHP :

```sh
php -S 127.0.0.1:8000 -t public
```

Accédez à votre application via `http://127.0.0.1:8000`.

## 📂 Structure du projet

- **`src/`** → Code source (contrôleurs, entités, services…)
- **`templates/`** → Templates Twig pour les vues
- **`public/`** → Fichiers accessibles publiquement (CSS, JS…)
- **`config/`** → Configuration de Symfony
- **`migrations/`** → Migrations de la base de données
- **`tests/`** → Tests unitaires et fonctionnels

## ⚙️ Configuration

Modifiez les variables d'environnement dans `.env` :

```
APP_ENV=dev
APP_SECRET=your_secret_key
DATABASE_URL="mysql://user:password@127.0.0.1:3306/nom_de_la_bdd"
```

Pour appliquer les configurations :

```sh
php bin/console cache:clear
```

## 📜 Licence

Ce projet est sous licence **MIT**. Voir le fichier [`LICENSE`](LICENSE) pour plus de détails.
