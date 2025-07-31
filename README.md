# EKS GitOps CI/CD Pipeline 🚀  
A complete production-grade CI/CD pipeline using Jenkins, Docker, SonarQube, Trivy, ArgoCD, and AWS EKS — built for fully automated GitOps-based Kubernetes deployments.

## 🔧 Tech Stack
- **CI/CD**: Jenkins, GitHub, Maven
- **Containerization**: Docker, Docker Hub
- **Security & Quality**: SonarQube, Trivy
- **GitOps Deployment**: ArgoCD, Kubernetes (EKS)
- **Infrastructure**: AWS EC2, EKS, IAM, Security Groups
- **Scripting**: Shell, Groovy
- **Monitoring**: Slack/email notifications

## ✅ Key Features
- 🧪 **Build & Test**: Automates Maven build and unit tests on GitHub commits
- 🔍 **Code Analysis**: Enforces code quality using SonarQube
- 🔐 **Security Scanning**: Trivy scans Docker images before deployment
- 📦 **Dockerized Builds**: Pushes container images to Docker Hub
- ⚙️ **GitOps Workflow**: Uses ArgoCD to sync Kubernetes manifests from GitHub
- 📬 **Notifications**: Slack/email integration for build & deploy status
- 🔁 **Auto Deployment**: Jenkins triggers CD job to auto-update manifests and deploy to EKS


## 🚀 How It Works (Flow)
1. Developer pushes code → GitHub triggers Jenkins CI job
2. CI:
   - Maven build + test
   - SonarQube code analysis
   - Docker build + Trivy scan + Docker Hub push
3. CI ends → Jenkins triggers CD job via API
4. CD:
   - Updates `deployment.yaml` image tag in GitOps repo
   - ArgoCD detects change → deploys to EKS
5. Notifications sent after successful deploy

## 🧪 Demo
<p align="center">
  <img src="https://github.com/yerragondu/EKS-GitOps-Pipeline/blob/main/Images/Screenshot%202025-07-30%20210911.png" width="600"/>
</p>
<p align="center">
  <img src="https://github.com/yerragondu/EKS-GitOps-Pipeline/blob/main/Images/Screenshot%202025-07-30%20210712.png" width="600"/>
</p>
## 👨‍💻 Try It Yourself
1. Fork the repo
2. Edit Jenkinsfiles to match your credentials
3. Follow the [YouTube guide](https://youtu.be/your-link) if needed
4. Run `git push` and watch the pipeline go!

## 📜 License
MIT

## 🙌 Acknowledgement
Inspired by [Ashfaque's CI/CD tutorial](https://youtu.be/your-link)
