# ⚙️ Cloud-Native billing-app-cicd-k8s – DevOps Project

![tech](https://img.shields.io/badge/stack-Docker%20|%20K8s%20|%20Jenkins%20|%20Prometheus-blue)

## 🚀 Descripción
Proyecto de ejemplo para mi portafolio: una **aplicación de facturación (Billing App)** que demuestra un flujo completo de **DevOps**.  
Incluye persistencia con **PostgreSQL**, empaquetado con **Docker**, pipeline de **CI/CD con Jenkins**, análisis de calidad con **SonarQube**, y despliegue/orquestación con **Kubernetes (Minikube)**. También incorpora monitoreo con **Prometheus + Grafana**.

---

## 🏗 Arquitectura general
- **Aplicación Billing**: API REST (o microservicio) con rutas CRUD para facturas, clientes y pagos.  
- **PostgreSQL**: persistencia de datos.  
- **Docker / Docker Compose**: contenedores locales para app, DB, SonarQube y Jenkins (opcional).  
- **Jenkins**: pipeline CI/CD (build, test, análisis Sonar, build imagen, push, deploy).  
- **Kubernetes (Minikube)**: despliegue en cluster local (Deployment, Service, ConfigMap, Secret, PVC).  
- **Prometheus + Grafana**: scraping de métricas y dashboards.

---

## 🔧 Tecnologías (ejemplos)
- Lenguaje: **(Node.js / Python / Java — especificar)**  
- Base de datos: **PostgreSQL**  
- Contenedores: **Docker**, **Docker Compose**  
- CI/CD: **Jenkins** (Jenkinsfile)  
- Calidad: **SonarQube**  
- Orquestador: **Kubernetes (Minikube)**  
- Monitoreo: **Prometheus**, **Grafana**  
- Repo: **GitHub**

---

## 🛠 Pipeline CI/CD (resumen de etapas)
1. Checkout del repositorio  
2. Instalación de dependencias  
3. Tests unitarios / integración  
4. Análisis de código con SonarQube  
5. Build de la aplicación (si aplica)  
6. Build de imagen Docker  
7. Push a registry (DockerHub / GitHub Container Registry)  
8. Despliegue en Kubernetes (apply manifests / Helm)  
9. Post-deploy checks y monitorización

---

## 📁 Estructura propuesta del repositorio

```
cloud-native-billing-app/
├── app/ # Código fuente de la aplicación
├── docker/ # Dockerfiles, scripts de build
├── docker-compose.yml # (opcional) entorno local
├── jenkins/
│ └── Jenkinsfile
├── k8s/ # Manifests: deployment, service, ingress, pvc, secrets
├── monitoring/ # Prometheus + Grafana configs / dashboards
├── sonar/ # Config SonarQube (properties)
├── charts/ # Helm charts (opcional)
├── tests/ # Tests e2e / integración
└── README.md
```
---

## 🔐 Configuración esencial (placeholders)
- Reemplazar `YOUR_DOCKERHUB_USER` y `YOUR_GITHUB_USER` en el Jenkinsfile y scripts.  
- Variables sensibles en **Kubernetes Secrets** o Jenkins Credentials (DB_PASSWORD, JWT_SECRET, etc.).  
- ConfigMaps para configuración no sensible (DB_HOST, DB_PORT, ENV variables).

---

## 📦 Ejemplos de comandos útiles

**Build y ejecución local con Docker Compose**
```bash
docker-compose build
docker-compose up -d
```
---
•
•
•
•
•
•
•

## 🚧Proyecto en construcción🚧⌚

