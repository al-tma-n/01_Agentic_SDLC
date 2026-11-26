# Challenge 1 - Dev environment, Copilot access & repo overview

**[Home](../README.md)** - [Next Challenge](challenge-02.md)

## Goal

Configure a working environment, confirm GitHub Copilot access, and become familiar with the **Octocat Supply** application before making changes.

## Actions

* **Open this standalone repository** — Use GitHub Codespaces, reopen it in the included VS Code Dev Container (`.devcontainer/`), or clone it locally. Confirm you are on the branch you intend to use; no special event account or fork naming convention is required.
* **Verify runtimes** — Confirm Node.js for the frontend and the runtime for your selected API track are available. The Codespace/Dev Container provides Node.js 24, Python 3.13, .NET 10, and Java 17.
* **Enable GitHub Copilot** — Sign in and confirm Copilot is entitled and responding in your IDE.
* **Explore the repository** — Review `src/` (frontend, four API variants, and shared SQLite schema), `src/docs/` (architecture and build guidance), `assets/` (Challenge 3 inputs), `.github/` (Copilot instructions and agent), and `scripts/` (optional backlog seeding). Read `src/README.md` for structure and commands.
* **Run the app locally** — Install/build as needed, then start the frontend and one API to confirm a baseline.

## Success criteria

* This repository is open in your chosen environment and Copilot is active.
* The frontend and at least one API build and run locally.
* You can describe how the frontend, selected API, and shared database fit together.

### Optional stretch — repo-wide agent context

Give Copilot persistent context for later challenges:

* Review the existing `.github/copilot-instructions.md` and path-specific instructions.
* Record the exact build and test commands for your selected API track and the frontend.
* Add scoped rules for generated files and unrelated services, then keep the resulting diff minimal.
* In a fresh Copilot Chat, ask a repository question and confirm the instructions influence the answer.

## Learning resources

* [Setting up GitHub Copilot](https://docs.github.com/en/copilot/quickstart)
* [GitHub Codespaces](https://docs.github.com/en/codespaces/overview)
* [Development Containers](https://containers.dev/)
* [Adding repository custom instructions for Copilot](https://docs.github.com/en/copilot/customizing-copilot/adding-repository-custom-instructions-for-github-copilot)
