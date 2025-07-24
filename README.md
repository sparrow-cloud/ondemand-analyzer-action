# 🔍 Analyze Repository GitHub Action

This GitHub Action analyzes a target GitHub repository via external API and updates the README with a summary table.

## 📥 Inputs

| Name         | Required | Description                          |
|--------------|----------|--------------------------------------|
| `ondemand_api_key`| ✅       | Sparrow On-Demand generated API-KEY |
| `repo_url`   | ✅       | URL of the repository to analyze     |
| `branch`     | ❌       | Branch to checkout                   |
| `vcs_auth_token`| ❌       | PAT(Public Access Token) for access Github private repo |

## 📤 Outputs

| Name           | Description                          |
|----------------|--------------------------------------|
| `result_summary`  | The raw result JSON returned by the API |
| `report_path`  | The report of Sparrow On-Demand Analysis result summary |

## ▶️ Example Usage

```yaml
- uses: sparrow-cloud/ondemand-analyzer-action@main
  with:
    ondemand_api_key: ${{ secrets.SPARROW_ONDEMAND_API_KEY }}
    repo_url: https://github.com/sparrow-cloud/ondemand
    branch: dev/2508.1
```
