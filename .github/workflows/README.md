# GitHub Actions Workflows

This directory contains the CI/CD workflows for the repository.

## Required repository settings

Set the following in GitHub repository settings before enabling the workflows:

- Secret: `AWS_CODEBUILD_ROLE_ARN` for the CodeBuild OIDC role
- Variable: `CODEBUILD_PROJECT_NAME` (optional, defaults to `codebuild-project`)
- Variable: `AWS_REGION` (optional, defaults to `us-east-1`)
- Variable: `ROLE_DURATION_SECONDS` (optional, defaults to `7200`)
- Variable: `DO_NOT_MERGE_LABEL` (optional, defaults to `do-not-merge`)

## Notes

- The release workflows depend on the `release` and `rules` labels being present when creating release PRs.
- PR validation workflows use the repository default `GITHUB_TOKEN` and do not require extra secrets for basic operation.
