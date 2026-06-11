# hssi-copilot-agents

GitHub Copilot CLI agents for managing [HSSI](https://hssi.hsdcloud.org) software metadata — extraction, validation, submission, and updates.

## Agents

- **Orchestrator** (.github/copilot-instructions.md) — Routes requests, manages pipelines, handles approval gates
- **Extractor** (.github/agents/hssi-metadata-extractor.agent.md) — Extracts metadata from repos into hssi_metadata.md
- **Validator** (.github/agents/hssi-metadata-validator.agent.md) — Independently validates extracted metadata
- **Submitter** (.github/agents/hssi-metadata-submitter.agent.md) — Builds API payloads and submits to HSSI
- **Updater** (.github/agents/hssi-metadata-updater.agent.md) — Updates existing HSSI entries with fresh metadata

Supporting skills live in `.github/skills/` and are loaded automatically when relevant.

## Steps to Use

1. Get [GitHub Copilot CLI](https://docs.github.com/copilot/how-tos/set-up/install-copilot-cli)
2. Clone this repo
3. Run `copilot` from the root dir
4. Point it to a software repo (e.g. local folder path, GitHub URL, DOI)
5. Metadata gets extracted into `repos/<repo>/hssi_metadata.md`
6. Optionally: ask Copilot to submit the metadata to HSSI (production or localhost)
7. To update existing entries: ask Copilot to e.g. "update sunpy on HSSI"

(Note: for the best results, always use the most capable available model on the highest reasoning setting—via `/model`)

## Other versions

This repo is the GitHub Copilot CLI version. Equivalent versions exist for other agent CLIs:

- [Claude Code version](https://github.com/Heliophysics-Software-Search-Interface/hssi-claude-agents)
- [Codex CLI version](https://github.com/Heliophysics-Software-Search-Interface/hssi-codex-agents)
