# student-list 
This repo is a simple application to list student with a webserver (PHP) and API (Flask)

![project](https://user-images.githubusercontent.com/18481009/84582395-ba230b00-adeb-11ea-9453-22ed1be7e268.jpg)


------------


### Person:

Firstname : Junior

Surname : Mbogning

For Eazytraining's 17th DevOps Bootcamp

LinkedIn : https://www.linkedin.com/in/juniormbogning/

Site : https://mbogning.com/


### Application:
L'application "student_age" que j'ai déployée est une solution simple composée de deux modules distincts :

API REST (avec authentification de base) :

Cette composante propose une interface de programmation pour récupérer la liste des ages des étudiants. Elle exige une authentification de base afin d'accéder aux données, qui sont extraites d'un fichier JSON servant de source pour la liste des étudiants.
Application Web (HTML + PHP) :

Le deuxième module est une interface utilisateur web développée en HTML et PHP. Les utilisateurs finaux peuvent interagir avec cette interface pour obtenir la liste des ages des étudiants de manière conviviale.
L'architecture modulaire de cette application assure une distinction claire entre la logique backend de récupération des données (via l'API REST) et la présentation des données à l'utilisateur (via l'application web). L'utilisation de l'authentification de base pour l'API renforce la sécurité en restreignant l'accès aux informations des étudiants uniquement aux utilisateurs autorisés. Si vous avez des interrogations spécifiques ou des points à clarifier, n'hésitez pas à les mentionner pour obtenir une assistance plus précise.

## Le besoin

Création d'un conteneur dédié à chaque module :

1. Mon rôle était de concevoir des conteneurs distincts pour chacun des modules. Chaque conteneur a été développé de manière à encapsuler efficacement les composants spécifiques, favorisant ainsi la portabilité et la gestion simplifiée.
Facilitation de l'interaction entre les modules :

2. J'ai mis en place un mécanisme permettant une communication harmonieuse entre les différents conteneurs. Cette interconnexion était cruciale pour assurer un échange de données fluide entre l'API REST et l'application web, garantissant ainsi la cohérence du système.
Mise en place d'un registre privé :

3. Mon travail a également inclus la création d'un registre privé, agissant comme un référentiel centralisé. Ce registre a été conçu pour stocker les images des conteneurs, assurant un contrôle d'accès strict et une gestion efficace des versions. Ceci renforce la sécurité et la confidentialité des informations stockées.

## Plan d'action

Dans un premier temps, permettez-moi de vous présenter les six fichiers qui composent ce projet, en détaillant leur fonction respective. Ensuite, je vous décrirai comment j'ai élaboré et évalué l'architecture pour argumenter mes choix. Enfin, la troisième et dernière section abordera la procédure de mise en service que je préconise pour cette application.

### Rôle des fichiers

Dans le livrable que je vous fournis, vous découvrirez trois fichiers principaux : un ***Dockerfile***, un ***docker-compose.yml***, et un ***docker-compose.registry.yml***.

- **docker-compose.yml :** Ce fichier est destiné à lancer l'ensemble de l'application, englobant à la fois l'API et l'application web.
  
- **docker-compose.registry.yml :** Son rôle est de mettre en route le registre local ainsi que son interface utilisateur.

- **simple_api/student_age.py :** Ce fichier renferme le code source de l'API, écrit en Python.

- **simple_api/Dockerfile :** Utilisé pour construire l'image de l'API en incorporant le code source à l'intérieur.

- **simple_api/student_age.json :** Contient les informations sur les étudiants, à savoir leurs noms et âges, formatés en JSON.

- **index.php :** Cette page PHP représente l'interface à laquelle l'utilisateur final se connectera pour interagir avec le service, permettant ainsi de répertorier les étudiants avec leurs âges.


## Pour la mise en place et les tests, suivez ces étapes 

Une fois le dépôt cloné, veuillez suivre ces étapes pour préparer l'application 'student_list':

Naviguez vers le répertoire approprié et procédez à la construction de l'image du conteneur API en utilisant les commandes suivantes :

```bash
cd ./mini-projet-docker/simple_api
docker build . -t api.student_list.img
docker images
```
![Capture d’écran du 2024-01-12 17-44-57](https://github.com/Mbogning/eazytraining-docker-project/assets/32342225/42893a1b-e99a-4079-84ce-c56e12b8f6b0)

