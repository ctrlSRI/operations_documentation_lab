# Agent Instructions — Operations Documentation Lab

## Purpose and boundaries

This repository is a **docs-as-code systems administration learning lab** and public technical-writing portfolio. It currently documents a local Windows 11 Pro / Hyper-V and Windows Server 2022 Evaluation environment; Linux/Ubuntu Server material is planned. **The repository documents lab procedures; it is not an authorization to manage live infrastructure.**

Read `README.md`, `docs/index.md`, and relevant topic files before making changes. Treat setup details in existing documentation as **historical lab context**, not as verified current machine state.

## Content organization

- Preserve the existing repository structure: `docs/windows-server/{tutorials,how-to,explanation,reference}/`, the corresponding Ubuntu Server hierarchy when established, and `screenshots/`.
- **Tutorials** are guided learning paths; **how-to guides** solve a particular task; **explanations** teach concepts; **reference pages** document commands and settings.
- Prefer editing the relevant existing guide rather than creating a new file for every command or question.
- Use Markdown, descriptive filenames, correctly resolved relative links, and appropriately redacted screenshots. Update `docs/index.md`, `README.md`, and `CHANGELOG.md` only when relevant to the change.
- Avoid copying long generic theory already documented in `ctrlSRI/IT-Knowledge-Base`; cross-link public reusable knowledge when appropriate. Keep lab-specific steps and observed results here.
- Explain abbreviations on first use, for example DNS (Domain Name System), DHCP (Dynamic Host Configuration Protocol), GPO (Group Policy Object), AD DS (Active Directory Domain Services), and NTFS (New Technology File System).

## Technical accuracy and reproducibility

- Distinguish **verified lab observations** from expected output, illustrative examples, hypotheses and proposed exercises. Never claim an unobserved step, test result or system configuration was verified.
- State prerequisites, environment and privileges; label commands **For PowerShell**, **For Git Bash**, or **For Linux shell** rather than mixing syntaxes.
- Document what every important command does, its effects, expected output, interpretation, and a safe rollback/recovery path where applicable.
- Separate non-destructive inspection commands from commands that change network adapters, virtual switches, DNS, DHCP, accounts, firewall rules, storage, services, policies or virtual machines.
- Do not execute disruptive commands, reconfigure networking or delete VMs/data without explicit user authorization. Prefer snapshots/checkpoints and tested recovery procedures when appropriate; checkpoints are not a substitute for backups.
- Treat hostnames, IP addresses and screenshots as potentially identifying: use fictional or sanitized examples unless the value is clearly safe to publish. Never publish credentials, tokens, private keys or secrets.

## Teaching and troubleshooting

- For interactive lab instruction provide **one actionable step at a time**, explain the command, show expected output and possible interpretations, and wait for the user's real output before proceeding.
- Troubleshooting entries should include **symptom → environment → observations → hypotheses → diagnostic steps → confirmed cause/fix (only if proven) → verification**.
- Maintain concise command-reference entries with a short purpose description as knowledge is verified. Do not label a suggested solution as successful without observing the actual result.
- Preserve the distinction between the user's production hardware/network and the isolated lab; do not assume permission to operate external systems.

## Updating documentation directly from a topic chat

The user may request documentation **from the same chat where the learning or troubleshooting occurred**. They do not need to copy the findings into a central documentation chat.

When explicitly instructed to update this repository:

1. Use only the conversation evidence actually available, plus authorized source files and repository access. Do **not** presume access to other chats, local workstations, screenshots or private files that were not supplied.
2. Extract reusable procedures, diagnostic patterns, relevant commands and **observed** results; omit conversational filler, private information and unverified success claims.
3. Read existing topic guides first. Extend the correct tutorial, how-to, explanation or reference document and update useful indexes/links.
4. Check relative links, formatting, version/platform claims, command effects and accidental sensitive information. Explain any verification limitations.
5. Create a descriptively named feature branch from the current **`master`** branch, unless the repository's default branch has changed.
6. Commit and push **only when the user has requested repository edits or a pull request**. Open a Pull Request to the correct default branch, report changed files and review notes, and **never merge automatically**.
7. Do not force-push, rewrite tags, delete files, or make unrelated changes without separate explicit authorization.

If repository access is unavailable, provide a proposed patch/Markdown instead of claiming the change was committed. No background or automatic cross-chat synchronization exists.

**Short request example:** "Document the relevant verified findings from this lab chat in `ctrlSRI/operations_documentation_lab`; follow AGENTS.md and create a PR without merging."

## Language and collaboration

Write documentation in clear English unless the user specifies otherwise. Respond in the language of the current conversation. For hands-on learning, label file content separately from commands and explanation. Preserve user control over merges and significant infrastructure actions.
