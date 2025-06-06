# GitHub Actions Workflow with Docker & Helm CI

# Project Overview:

This repository demonstrates how to extend a GitHub Actions workflow with CI
steps for building and pushing Docker images, and for validating and packaging
Helm charts. The CI is configured to run only on the personal feature branch
(your_name), not on main.

# Tech Stack:

- GitHub Actions (CI/CD)
- Docker & DockerHub
- Helm
- GitHub Repository Secrets
- GitHub Actions Artifacts

# What Was Done:

- Added a docker-ci job to build and push Docker images to DockerHub.
- Helm CI:
  - Added a helm-ci job that runs after Docker CI.
  - helm-ci includes:
    - Downloading Helm artifacts.
    - Running helm template to validate rendered manifests.
    - Running helm lint to check chart syntax and structure.
    - Packaging the Helm chart.
    - Uploading the .tgz chart archive to GitHub Actions artifacts.
    - helm-ci also runs only on the your_name branch.


# Link to the successful GitHub Actions run:
https://github.com/konstantinou77/devops_todolist_cicd_task_4_helm_ci/actions/runs/14729288873

