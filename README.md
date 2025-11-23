# Julia reusable workflows
Reusable GitHub workflows for Julia notebook publishing projects.

Source:

- [GitHub reusable workflows](https://docs.github.com/en/actions/how-tos/reuse-automations/reuse-workflows)

## Jupyter Book + parallel matrix

## Update `Manifest.toml`

```yaml
jobs:
  update:
    permissions:
      contents: write
      pull-requests: write
    uses: ww-jl/actions/.github/workflows/update-manifest.yml@main
    secrets:
      personal_access_token: ${{ secrets.PAT }}
```

This workflow needs a personal access token (PAT) with `repo` write access. Or one can [authenticate with a custom GitHub APP](https://github.com/peter-evans/create-pull-request/blob/main/docs/concepts-guidelines.md#authenticating-with-github-app-generated-tokens).
