# PR-Agent with Kaito Integration

This repository demonstrates how to run PR-Agent with Kaito as the backend for code review automation. It includes:

- A Kubernetes Deployment to run PR-Agent using Kaito.
- A Docker script for local testing.
- A GitHub Action for automated reviews.

---

Setup & Usage
1. Run with Docker
For quick testing, use the script below:

```bash
chmod +x scripts/run_docker.sh
./scripts/run_docker.sh
```

2. Run in Kubernetes
Apply the job manifest:
```bash
kubectl apply -f config/pr-agent-job.yaml
```

3. Run in GitHub Actions

Use the provided workflow in `.github/pr-review.yaml` to automate PR reviews.

---

Configuration
In all setups, replace the following placeholders with your actual values:

- OLLAMA_API_BASE → Your Kaito workspace URL.
- GITHUB_USER_TOKEN → Your GitHub API token.
- PR_URL → The pull request URL to review.

Ensure these values are correctly set in your Docker environment, Kubernetes job, or GitHub Actions workflow before running.
