# DevSecOps Pipeline – Conceptual Project

This repository represents my learning journey into DevSecOps using a practical CI/CD pipeline approach.

## What is DevSecOps?

DevSecOps follows a shift-left mindset by embedding security checks early in the development process and automating them within CI/CD pipelines, instead of fixing security issues at the end.

## Pipeline Flow

Developer Commit (GitHub) -> CI Trigger (Jenkins) -> Build & Unit Tests -> Static Code Analysis (SAST – SonarQube) -> Dependency & Image Scan (SCA – Trivy) -> Dynamic Security Testing (DAST – OWASP ZAP) -> Artifact Packaging (Docker) -> Deployment (AWS – conceptual)

## Tools Used (Conceptual)

| Pipeline Stage   | Tool          | Why it is used                                           |
|------------------|---------------|----------------------------------------------------------|
| Source Control   | GitHub        | Stores code and triggers CI pipeline                     |
| CI Orchestration | Jenkins       | Automates build, test, and security stages               |
| Build & Test     | Node.js / npm | Builds application and runs unit tests                   |
| SAST             | SonarQube     | Detects code quality issues and security vulnerabilities |
| SCA              | Trivy         | Scans dependencies and container images for known CVEs   |
| DAST             | OWASP ZAP     | Identifies runtime security vulnerabilities              |
| Containerization | Docker        | Packages application into deployable images              |
| Deployment       | AWS           | Hosts the application (conceptual)                       |

## Pipeline Explanation

1. **Developer Commit (GitHub)**
   The developer pushes code to GitHub, which acts as the single source of truth and triggers the CI pipeline.

2. **CI Trigger (Jenkins)**  
   Jenkins automatically starts the pipeline when changes are detected in the repository.

3. **Build & Unit Tests**  
   The application is built and unit tests are executed to ensure basic functionality before proceeding further.

4. **Static Code Analysis (SAST – SonarQube)**  
   SonarQube analyzes the source code to detect code smells, bugs, and security vulnerabilities early in the pipeline.

5. **Dependency & Image Scan (SCA – Trivy)**  
   Trivy scans project dependencies and container images to identify known vulnerabilities (CVEs).

6. **Dynamic Security Testing (DAST – OWASP ZAP)**  
   OWASP ZAP scans the running application to identify runtime vulnerabilities such as injection flaws and misconfigurations.

7. **Artifact Packaging (Docker)**  
   The validated application is packaged into a Docker image to ensure consistency across environments.

8. **Deployment (AWS – conceptual)**  
   The Dockerized application is deployed to the hosting environment.

## Current Status

- CI/CD pipeline design and security flow documented
- Implementation will be completed incrementally with hands-on stages

