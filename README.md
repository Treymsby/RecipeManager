# Recipe Manager 🍲

A **self-hosted Recipe Manager web application** designed to run in containers and Kubernetes.
It provides a modern web UI for managing recipes, ingredients, and images, backed by a REST API and PostgreSQL.

The project is built with **open-source, free technologies** and is intended for personal or small-team use.

---

## Features

* Web-based recipe management
* Create, edit, delete, and view recipes
* Ingredients with quantities and units
* Tags / categories
* Image uploads for recipes
* Search and filtering
* User authentication (JWT)
* Self-hosted & containerized
* Kubernetes-ready deployment

**Planned / Optional**

* Offline access (PWA)
* Meal planning & shopping lists
* Import/export recipes
* Multi-user support
* Native mobile app (future)

---

## Tech Stack

### Frontend

* React (JavaScript)
* Vite
* React Router
* React Query
* UI Library (Material UI or Mantine)

### Backend

* Node.js
* Express (or NestJS)
* Prisma ORM
* REST API

### Database

* PostgreSQL

### Infrastructure

* Docker
* Kubernetes
* Helm or Kustomize
* NGINX Ingress or Traefik
* cert-manager (TLS)

**Optional**

* MinIO (S3-compatible storage for images)

---

## Architecture Overview

```
Browser (React Web App)
        |
        v
REST API (Node.js)
        |
        v
PostgreSQL
```

All components run in containers and can be deployed locally with Docker or to a Kubernetes cluster.

---

## Getting Started (Development)

### Prerequisites

* Docker
* Docker Compose
* Node.js (for local development without containers)

### Local Development

```
git clone https://github.com/yourusername/recipe-manager.git
cd recipe-manager
docker compose up --build
```

* Web App: [http://localhost:3000](http://localhost:3000)
* API: [http://localhost:4000](http://localhost:4000)
* Database: PostgreSQL (internal container)

---

## Kubernetes Deployment

Kubernetes manifests or Helm charts are located in:

```
deploy/
  k8s/
```

Basic steps:

1. Create secrets (database password, JWT secret)
2. Apply manifests or install via Helm
3. Configure ingress and domain
4. (Optional) Enable TLS with cert-manager

---

## Offline Support

The web app can optionally be configured as a **Progressive Web App (PWA)**:

* Recipes can be cached for offline viewing
* Full offline editing is planned for future versions

---

## Project Goals

* 100% self-hosted
* No vendor lock-in
* Fully open-source stack
* Easy to deploy and maintain
* Extendable for future mobile apps
* Deploy Via CICD

---

## License

MIT License

You are free to use, modify, and distribute this project.

---

## Contributing

Contributions are welcome:

* Bug reports
* Feature requests
* Documentation improvements
* Code contributions

Please open an issue or pull request.

---

## Disclaimer

This project is under active development.
Features, APIs, and database schemas may change.

---

If you want, I can also:

* Adjust this for **Express-only** or **NestJS-only**
* Make it **PWA-first**
* Add **Docker / Kubernetes badges**
* Rewrite it for a **public open-source audience** or **private self-hosted use**

Just tell me.

