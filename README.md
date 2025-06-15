# BobApp

## 📑 Présentation

BobApp est un projet démontrant la mise en place complète d’une chaîne CI/CD professionnelle avec :

- Backend : Spring Boot (Java 11)
- Frontend : Angular
- Intégration continue : GitHub Actions
- Analyse de qualité : SonarCloud
- Déploiement de conteneurs : Docker + Docker Hub

L’objectif est de valider automatiquement le code, assurer sa qualité et déployer les images sur un registre Docker.

---

## 🔧 Technologies utilisées

- **Backend** : Java 11, Spring Boot, Maven
- **Frontend** : Angular, Node.js, npm
- **CI/CD** : GitHub Actions
- **Analyse qualité** : SonarCloud
- **Tests** : JUnit (Back), Karma/Jasmine (Front)
- **Couverture de tests** : Jacoco (Back), lcov (Front)
- **Docker** : DockerHub (Public Registry)

---

## 🚀 Workflows CI/CD mis en place

### ✅ CI Frontend (`.github/workflows/ci-front.yml`)

- Installation des dépendances
- Exécution des tests unitaires et génération de la couverture de code
- Analyse qualité SonarCloud

### ✅ CI Backend (`.github/workflows/ci-back.yml`)

- Build et tests Maven
- Génération du rapport de couverture Jacoco
- Analyse qualité SonarCloud

### ✅ CD DockerHub (`.github/workflows/cd-dockerhub.yml`)

- Build des images Docker Front et Back
- Push automatique des images sur Docker Hub :
    - `hamdene/bobapp-front:latest`
    - `hamdene/bobapp-back:latest`

---

## 🔐 Gestion des secrets GitHub Actions

Les secrets suivants sont configurés dans le repository :

| Secret Name | Description |
|--------------|-------------|
| `SONAR_TOKEN` | Token d’accès SonarCloud |
| `SONAR_HOST_URL` | URL de SonarCloud |
| `DOCKERHUB_USERNAME` | Username Docker Hub |
| `DOCKERHUB_TOKEN` | Token personnel Docker Hub |

---

## 📊 Métriques obtenues (exemple de la dernière exécution)

| Application | Coverage | Quality Gate |
|--------------|----------|---------------|
| Frontend     | 83.3%    | Passed        |
| Backend      | 38.8%    | Passed        |


---

## 📎 Liens utiles

- [Repository SonarCloud Frontend](https://sonarcloud.io)
- [Repository SonarCloud Backend](https://sonarcloud.io)
- [Docker Hub Frontend](https://hub.docker.com/r/hamdene/bobapp-front)
- [Docker Hub Backend](https://hub.docker.com/r/hamdene/bobapp-back)

---
