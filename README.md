# OpenSSL Windows build system powered by GitHub Actions (Test Sandbox Repo Archive)

## About
- `.github/workflows/build.yml` - Builds the OpenSSL git submodule every time a tag is added.
- `.github/workflows/update-openssl` - Checks for a new OpenSSL release tag daily and updates the submodule and adds a new release tag, triggering the Build workflow.

## How to configure
1. Enable the GitHub Actions workflows
2. A personal GitHub user token is used for the workflows to trigger each other. You will need to create a personal access token in the GitHub Developer Settings menu with the `public_repo` and `write:repo_hook` permissions. Then, add this token in your repo's Secrets and variables Settings menu as a secret with the name `PUSH_TOKEN`.
