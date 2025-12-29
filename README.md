# Jenkins Multibranch Pipeline

This repository demonstrates a **real-world Jenkins Multibranch Pipeline** implementation using **Pipeline-as-Code**.  
It shows how Jenkins automatically detects multiple Git branches and executes CI pipelines based on branch strategy.

---

## 📌 Project Objective

To implement an **enterprise-style CI setup** where:
- Jenkins automatically detects branches
- Pipelines run per branch using a `Jenkinsfile`
- Different branches represent different stages of development

---

## 🧱 Branch Strategy

The repository follows a standard industry branching model:

| Branch | Purpose |
|------|--------|
| `feature/*` | Feature development & testing |
| `develop` | Integration testing |
| `main` | Production-ready code |

Jenkins scans the repository and triggers pipelines **only for branches containing a Jenkinsfile**.

---

## 🔄 Jenkins Multibranch Pipeline Flow

```text
GitHub Repository
   ├── feature/*
   ├── develop
   └── main
        ↓
Jenkins Multibranch Pipeline
        ↓
CI Pipeline Execution
