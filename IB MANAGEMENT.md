---
tags : mod cs
---
Created: 2024-03-22

the idea for my web app: 
I want to create a react web app that manages grade report for the IB program and help manage them by class (11th and 12th grade) and students with each teacher being a user that can input there grades for their own class and the coordinator with accès to everything (will be the moderator). Students will also be able to get Access to there grade report and have automatic conversion in different format from french to GPA to English's grading system etc.... and people can download a pdf version all of this information stored in a central MySQL database with multiple tables for all info. The Teacher can set grade boundaries for their whole subject and for individual grades so that wen it is inputted in the app it is automatically converted to the IB grading format (over 7). The students can see there grades. There is also auto calculation of average and show worst and best grade anonymously.
All of this i am planning to use java-script react and node.js MySQL for the database. My code interpreter is VS code.

### Database Schema

1. **Users Table** (For storing user information including teachers, students, and coordinators)
    
    - `user_id` INT AUTO_INCREMENT PRIMARY KEY
    - `username` VARCHAR(255) UNIQUE NOT NULL
    - `password` VARCHAR(255) NOT NULL
    - `role` ENUM('teacher', 'student', 'coordinator') NOT NULL
    - `full_name` VARCHAR(255) NOT NULL
2. **Classes Table** (For storing class details)
    
    - `class_id` INT AUTO_INCREMENT PRIMARY KEY
    - `class_name` VARCHAR(255) NOT NULL
    - `grade_level` ENUM('11', '12') NOT NULL
    - `subject` VARCHAR(255) NOT NULL
    - `teacher_id` INT, FOREIGN KEY REFERENCES `Users`(`user_id`)
3. **Grades Table** (For storing grades of students)
    
    - `grade_id` INT AUTO_INCREMENT PRIMARY KEY
    - `student_id` INT, FOREIGN KEY REFERENCES `Users`(`user_id`)
    - `class_id` INT, FOREIGN KEY REFERENCES `Classes`(`class_id`)
    - `grade_value` DECIMAL(5,2) NOT NULL
    -  `total_value` DECIMAL(5,2) NOT NULL AFTER
    - `trimester` ENUM('1', '2', '3') NOT NULL
4. **GradeBoundaries Table** (For storing grade boundaries for subjects)
    
    - `boundary_id` INT AUTO_INCREMENT PRIMARY KEY
    - `class_id` INT, FOREIGN KEY REFERENCES `Classes`(`class_id`)
    - `over_value` DECIMAL(5,2) NOT NULL AFTER
    - `grades` TEXT NOT NULL
5. **StudentClasses Table** 

- `student_id` INT, FOREIGN KEY REFERENCES `Users(user_id) `
- `class_id` INT, FOREIGN KEY REFERENCES `Classes(class_id)`

Je veux normaliser ma base de données donc donne comme dans "Database Schema". tu peux voir l'exemplw :
Formes de normalisation 1NF, 2NF, 3NF 
 Procédure de normalisation : 
 Diviser en tables logiques distinctes (par entité) Exemple : Elève, Classe, Professeur sont des entités distinctes Qu'est-ce qui est associé UNIQUEMENT à chaque entité ? 
 Pour déterminer les attributs pour chaque entité Se débarrasser de tous les attributs ayant des valeurs multiples en créant de nouvelles tables Exemple : Plusieurs notes pour l’entité élève => Création de la table Evaluation S'assurer qu'aucun attribut ne dépend d'UNE clé primaire - sinon, créer une nouvelle table. 
 S'assurer qu'aucun attribut ne dépend d'un autre attribut non clé primaire, sinon créer une nouvelle table. 
 S’assurer que les tables sont toutes liées par des relations (clé primaire → clé étrangère). 
 S’assurer que chaque table possède une clé primaire.
