## 📚 Job 1 - Création d'une base de données MySQL pour un établissement scolaire

### 📝 Objectif

Ce projet a pour but de créer une base de données nommée `jobsql` contenant les informations d'étudiants, d'étages et de salles, puis d'y insérer des données précises.

---

### 🛠️ Outils utilisés

- [phpMyAdmin](https://www.phpmyadmin.net/) ou tout autre SGBD compatible MySQL/MariaDB
- MySQL/MariaDB Server
- Exportation SQL (.sql)

---

### 📁 Contenu du dépôt

- `job01.sql` : Export de la base de données vide avec uniquement les tables créées.
- `job02.sql` : Export de la base de données avec les données insérées.
- `README.md` : Fichier d'explication du projet.

---

### 🧱 Structure de la base de données

### Base de données : `jobsql`

### Tables :

#### 1. `etudiants`
| Champ     | Type         | Description                      |
|-----------|--------------|----------------------------------|
| id        | INT          | Clé primaire, auto-incrémentée   |
| prenom    | VARCHAR(255) | Prénom de l'étudiant             |
| nom       | VARCHAR(255) | Nom de famille                   |
| naissance | DATE         | Date de naissance                |
| sexe      | VARCHAR(25)  | Sexe                             |
| email     | VARCHAR(255) | Adresse email                    |

#### 2. `etage`
| Champ       | Type         | Description                      |
|-------------|--------------|----------------------------------|
| id          | INT          | Clé primaire, auto-incrémentée   |
| nom         | VARCHAR(255) | Nom de l'étage (RDC, R+1, etc.)  |
| numero      | INT          | Numéro de l'étage                |
| superficie  | INT          | Superficie en m²                 |

#### 3. `salles`
| Champ      | Type         | Description                         |
|------------|--------------|-------------------------------------|
| id         | INT          | Clé primaire, auto-incrémentée      |
| nom        | VARCHAR(255) | Nom de la salle                     |
| id_etage   | INT          | Clé étrangère liée à `etage.id`     |
| capacite   | INT          | Capacité d'accueil de la salle      |

---

## ✅ Étapes réalisées

### Job 1

1. Création de la base de données `jobsql`.
2. Création des tables `etudiants`, `etage`, et `salles`.
3. Export rapide de la base : `job01.sql`.

### Job 2

1. Insertion de 7 étudiants dans la table `etudiants`.
2. Insertion de 3 étages dans la table `etage`.
3. Insertion de 14 salles dans la table `salles`.
4. Nouvelle exportation rapide de la base avec les données : `job02.sql`.

---

## 💾 Utilisation

1. Importez `job01.sql` ou `job02.sql` via phpMyAdmin ou en ligne de commande :

```bash
mysql -u root -p jobsql < job01.sql


