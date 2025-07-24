# 🔍 Analyze Repository GitHub Action

This GitHub Action analyzes a target GitHub repository via external API and updates the README with a summary table.

## 📥 Inputs

| Name         | Required | Description                          |
|--------------|----------|--------------------------------------|
| `ondemand_api_key`| ✅       | Sparrow On-Demand generated API-KEY |
| `repo_url`   | ✅       | URL of the repository to analyze     |
| `branch`     | ❌       | Branch to checkout                   |
| `vcs_auth_token`| ❌       | Local directory (default: `target-repo`) |

## 📤 Outputs

| Name           | Description                          |
|----------------|--------------------------------------|
| `result_summary`  | The raw result JSON returned by the API |

## ▶️ Example Usage

```yaml
- uses: sparrow-cloud/ondemand-analyzer-action@main
  with:
    repo_url: https://github.com/sparrow-cloud/ondemand
    branch: dev/2508.1
```
