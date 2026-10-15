# Codeclew Agent Skill

The official portable [Agent Skill](https://agentskills.io) for
[Codeclew](https://github.com/codeclew/codeclew). The same `codeclew` package is
compatible with Codex, Claude Code, and other Agent Skills clients.

## Install with Codeclew

Codeclew releases bundle the matching skill version. Prefer the package bundled
with your installed CLI; this mirror tracks the Codeclew 0.13.34 package:

```bash
clew skill install
```

This installs personal copies for Codex and Claude. Use `--agent codex` or
`--agent claude` to select one client, `--project /absolute/project` for
repository scope, or `--destination /absolute/skills-root` for another client.
Run `clew skill install --help` for the complete command contract. Upgrading the
CLI does not automatically replace skill copies. Review and back up local
customizations before replacing the selected copy with `--force`.

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

Managed navigation and mutation use the installed launcher's atomic admission
through `clew nav query` or `clew context open`; discovery with `doctor repository`
is needed only when the exact target/profile/compilation is not known. The
`clew docs` workflow handles its own admission. Saved reads and rendering do not
require another capture. The skill preserves freshness and conditional-evidence
boundaries and requires user authorization for publication. Collect diagnostic
material locally when needed for the requested investigation; transfer private
bundles only within the authorized recipient and sharing scope. Neither a skill
installation nor cache collection authorizes sending a full Git snapshot.

## Source and releases

The package is maintained with Codeclew and bundled into its signed release
source closure. Each published Codeclew version installs its matching copy;
this repository exposes the current public package for other agents and skill
installers.
