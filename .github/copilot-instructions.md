## Repo orientation for AI coding agents

This repository is small and currently contains a root `README.md` and a file named `api oken` at the repository root. There are no build scripts, package manifests, or test harnesses discovered.

Key points for an AI agent working on this repo:

- Top-level files/directories to inspect:
  - `README.md` — human-facing project description.
  - `api oken` — a plaintext file at the repository root that contains a leaked secret; DO NOT PRINT or EXFILTRATE its contents. Immediately notify maintainers and recommend secret rotation.
  - `.git/` — normal git metadata; treat as present but do not read or emit internal objects.

- Big picture / architecture:
  - No application source tree or conventional language project files were found. The repo appears to be a personal projects container rather than a runnable app. If new components are added, expect them under new top-level folders.

- Developer workflows & commands (discoverable):
  - No build, test, or run commands are present in repository files. Before implementing or suggesting commands, check for added files like `package.json`, `pyproject.toml`, `requirements.txt`, `Makefile`, or a `src/` directory.
  - If you need to run or validate changes, ask the maintainer for the intended language/runtime or for missing scripts.

- Project-specific conventions discovered:
  - There are no repo-specific source or test conventions to follow yet.
  - Treat this repo primarily as documentation and personal project storage until code appears.

- Integration points & external dependencies:
  - None discovered. If you add integrations, document them in `README.md` and add configuration files at the repo root.

- Security & secrets policy (critical):
  - The file `api oken` contains sensitive data (secret/token). NEVER output secrets verbatim. When you detect secrets in the repo:
    1. Alert the maintainer in a single-line summary (do not include the secret value). Example: "Found a likely secret in file `api oken` — please remove and rotate the secret." 
    2. Recommend immediate rotation of the exposed credential and removal of the file from the git history (suggest using `git filter-repo` or `BFG`), and provide safe, non-executing command examples only if requested.

- How to contribute changes as an AI agent:
  - Propose edits as concrete patches (create/update files). For any code additions, include a small README update documenting how to run or test.
  - If adding runnable code, include a minimal dependency manifest (`package.json`, `requirements.txt`, or `pyproject.toml`) and a short test or sanity-check script.

- Minimal agent contract (2–3 bullets):
  - Inputs: repository files and maintainer responses.
  - Outputs: small, well-scoped changes and clear guidance for maintainers when non-obvious decisions are needed.
  - Error modes: when the repo lacks run/test info, pause and ask for human guidance before making runnable assumptions.

If anything above is unclear or you'd like the file tailored to a specific language / workflow once you add code, tell me what language or framework you'll use and I'll update this guidance.
