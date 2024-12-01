# AWS Deployment with Docker and GitHub Actions 💻

This project demonstrates a **continuous deployment workflow** to an AWS EC2 instance using **Docker** for containerization and **GitHub Actions** for automation. The deployed application is a static website served by **Nginx**.

---

## Features 🔥
- **Automated Builds**: GitHub Actions automates the build and push process for Docker images.
- **Containerization**: Packages the application into a lightweight Docker container.
- **AWS Deployment**: Automates the deployment to an AWS EC2 instance.
- **Continuous Deployment**: Ensures any changes pushed to the repository are live immediately.

---

## Project Structure 🛠️

```bash
.
├── .github/
│   └── workflows/
│       └── aws_deploy.yml      # GitHub Actions workflow file for deployment
├── index.html                  # Main HTML file for the project
├── styles.css                  # CSS file for styling the HTML page
├── Dockerfile                  # Dockerfile to containerize the project
└── README.md                   # Documentation for the project

```
## Workflow Explanation

1. **Build and Push Docker Image 📦**:
   - When code is pushed to the `main` branch, the workflow:
     - Checks out the code.
     - Builds a Docker image using the `Dockerfile`.
     - Pushes the image to Docker Hub.

2. **Deploy to AWS 🚀**:
   - SSHs into an AWS EC2 instance.
   - Installs Docker (if not already installed).
   - Pulls the latest Docker image from Docker Hub.
   - Runs the container, exposing it on port `80`.

### Explanation ⚙️:

This `README.md` provides a detailed description of the `Dockerfile` and its role in the deployment pipeline. It breaks down each command used in the `Dockerfile` and explains how they contribute to containerizing the web application. Additionally, it explains how the Docker image is used in the GitHub Actions workflow for automated deployment to AWS.

Let me know if you need further adjustments! 😊