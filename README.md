# Job-Concurrency

# 🚀 GitHub Actions — Job Concurrency Demo

This project demonstrates how **Job Concurrency** works in GitHub Actions to prevent duplicate workflow runs and optimize CI pipelines.

---

## 📌 What is Job Concurrency?

Job concurrency ensures that only the latest workflow execution runs while cancelling previous running jobs for the same branch.

This helps:

- Prevent duplicate builds
- Save CI minutes
- Reduce queue time
- Improve pipeline efficiency

---

## ⚙️ Concurrency Configuration

```yaml
concurrency:
  group: ${{ github.workflow }}-${{ github.ref }}
  cancel-in-progress: true
