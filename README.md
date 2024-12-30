# Hospital Management System

## Description
L'Hospital Management System est une application Java permettant de gérer les opérations essentielles d'un hôpital. Ce projet fournit une interface utilisateur graphique (GUI) pour gérer les patients, les médecins, les rendez-vous, et générer des rapports, tout en intégrant une base de données MySQL pour la persistance des données.

---

## Fonctionnalités

### 1. Authentification
- Un système de connexion sécurisé pour accéder au tableau de bord.
- Vérification des identifiants dans une base de données MySQL.

### 2. Tableau de bord
- Accès rapide aux fonctionnalités principales via des boutons clairs et organisés :
  - **Manage Patients** : Gérer les informations des patients (ajout, modification, suppression).
  - **Manage Doctors** : Gérer les informations des médecins (ajout, spécialités, etc.).
  - **Manage Appointments** : Planifier, reprogrammer et afficher les rendez-vous.
  - **Generate Reports** : Générer des rapports basés sur les données de l'hôpital.
  - **Logout** : Retourner à l'écran de connexion.

### 3. Gestion des données avec MySQL
- Les données des utilisateurs, patients, et médecins sont stockées dans une base de données MySQL.
- Utilisation de JDBC pour interagir avec la base de données.

### 4. Interface utilisateur conviviale
- Développée avec Java Swing pour une expérience utilisateur simple et intuitive.
- Utilisation de fenêtres séparées pour chaque fonctionnalité.

---

## Technologies utilisées
- **Langage** : Java
- **Interface utilisateur** : Java Swing
- **Base de données** : MySQL
- **Connecteur JDBC** : MySQL Connector/J
- **IDE recommandé** : IntelliJ IDEA, Eclipse

---

## Configuration requise

1. **Installer Java (JDK)** :
   - Assurez-vous que Java Development Kit (JDK) est installé.

2. **Installer MySQL** :
   - Créez une base de données `hospital` et configurez la table des utilisateurs :
     ```sql
     CREATE DATABASE hospital;
     USE hospital;
     CREATE TABLE users (
         id INT AUTO_INCREMENT PRIMARY KEY,
         username VARCHAR(50) NOT NULL,
         password VARCHAR(50) NOT NULL
     );
     INSERT INTO users (username, password) VALUES ('admin', 'admin123');
     ```

3. **Télécharger le MySQL Connector/J** :
   - Ajoutez le fichier `.jar` du connecteur à votre projet.

---

## Instructions d'installation

1. Clonez ce dépôt GitHub :
   ```bash
   git clone https://github.com/<votre-utilisateur>/hospital-management-system.git
   cd hospital-management-system
   ```
2. Ouvrez le projet dans votre IDE (IntelliJ IDEA, Eclipse).
3. Ajoutez le fichier `mysql-connector-java.jar` au chemin de classe.
4. Configurez la connexion MySQL dans le code :
   - Modifiez le nom d'utilisateur (`root`) et le mot de passe dans le fichier principal.
5. Exécutez le fichier `HospitalManagementSystem.java`.

---

## Améliorations futures
- Ajouter une table pour afficher les listes de patients, médecins, et rendez-vous.
- Intégrer des statistiques graphiques avec JFreeChart.
- Implémenter un système de gestion des rôles (admin, médecin, réceptionniste).
- Ajouter un système de notifications pour les rendez-vous à venir.

---

## Contribuer
Les contributions sont les bienvenues ! Si vous souhaitez contribuer, veuillez créer une demande d'extraction (pull request) ou ouvrir une issue pour discuter des modifications souhaitées.

---

## Licence
Ce projet est sous licence MIT. Consultez le fichier LICENSE pour plus de détails.

