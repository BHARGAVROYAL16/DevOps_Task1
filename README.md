# DevOps Task 1 - CI/CD Pipeline with GitHub Actions

## 🚀 Objective
This project demonstrates automating the deployment of a Node.js web application using a CI/CD pipeline powered by **GitHub Actions** and **Docker**. The final Docker image is pushed to **DockerHub** automatically on every push to the `main` branch.

---

## 🔧 Tech Stack
- Node.js
- GitHub Actions
- Docker
- DockerHub

---

    
---

## ⚙️ CI/CD Workflow Summary

### Trigger
- Runs automatically on every push to the `main` branch.

### Steps
1. **Checkout Code** – Clones the repository.
2. **Setup Node.js** – Installs the specified version.
3. **Install Dependencies** – Runs `npm install`.
4. **Run Tests** – Executes `npm test`.
5. **Build Docker Image** – Builds the Docker image using `Dockerfile`.
6. **Login to DockerHub** – Uses GitHub Secrets for authentication.
7. **Push Docker Image** – Pushes the image to DockerHub.

---

## 🐳 Docker

### Dockerfile
A simple Dockerfile is included to containerize the Node.js app:

```dockerfile
FROM node:16
WORKDIR /app
COPY . .
RUN npm install
EXPOSE 3000
CMD ["npm", "start"]


