# Codeclew Agent Skill

The official portable [Agent Skill](https://agentskills.io) for
[Codeclew](https://github.com/codeclew/codeclew). The same `codeclew` package is
compatible with Codex, Claude Code, and other Agent Skills clients.

## Install with Codeclew

Codeclew releases bundle the matching skill version:

```bash
clew skill install
```

This installs personal copies for Codex and Claude. Use `--agent codex` or
`--agent claude` to select one client, `--project /absolute/project` for
repository scope, or `--destination /absolute/skills-root` for another client.
Run `clew skill install --help` for the complete command contract.

## Install from GitHub

The installable skill directory is
[`codeclew`](https://github.com/codeclew/codeclew-skill/tree/main/codeclew).

- Codex users can ask `$skill-installer` to install that directory.
- Claude Code users can copy it to `~/.claude/skills/codeclew` or a project's
  `.claude/skills/codeclew` directory.
- Other compatible agents can import or copy the same directory into their
  configured Agent Skills root.

Restart an agent session if the client does not discover a newly installed
skill immediately.

## Safety contract

The skill admits a task only after canonical `clew capabilities` and `clew
doctor` checks, preserves freshness and conditional-evidence boundaries, and
requires explicit user approval before publication. It never authorizes broad
repository mutation or disclosure of private Codeclew diagnostics.

## Source and releases

The package is maintained with Codeclew and bundled into its signed release
source closure. Each published Codeclew version installs its matching copy;
this repository exposes the current public package for other agents and skill
installers.
