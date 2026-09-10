# SpecTrail PRD author skill

Turn ideas, discovery notes, feature requests, and existing drafts into reviewable PRDs. The skill adapts document depth, preserves the distinction between evidence and proposals, and checks requirements and binding constraints for verification.

## Portable package

```text
skills/prd-author/
├── SKILL.md
├── LICENSE
└── assets/
    └── prd-template.md
```

The entire `prd-author` directory is the installable unit. `dist/prd-author.zip` contains that directory for transfer. Extract it before using filesystem discovery; archive-import behavior depends on the host. A `.skill` extension is not required by the shared directory format.

The package uses standard `name`, `description`, and `license` frontmatter, Markdown instructions, and a relative asset path. It has no runtime dependencies, required network access, provider-specific tool names, or plugin manifest. The host must be able to load the instructions and read the bundled asset. This follows the [Agent Skills specification](https://agentskills.io/specification).

## Installation

Choose one route: Vercel's installer, manual folder installation, or ZIP download. Keep only one installed copy per intended scope to avoid ambiguity.

### Vercel's installer

Requires Node.js and npm (`npx`). Run from the project where you want to use the skill:

```bash
npx skills add mikeshuh/SpecTrail --skill prd-author
```

Follow the prompts to choose your agents and installation method. To target Codex and Claude Code explicitly:

```bash
npx skills add mikeshuh/SpecTrail --skill prd-author --agent codex claude-code
```

Installation is project-scoped by default. Add `--global` for personal installation across projects. Add `--list` to inspect available skills without installing. These options are documented by [Vercel's skills CLI](https://github.com/vercel-labs/skills).

You can also install from a local checkout by replacing the repository identifier with its actual path:

```bash
npx skills add /path/to/SpecTrail --skill prd-author
```

Source: [mikeshuh/SpecTrail](https://github.com/mikeshuh/SpecTrail). No npm package for SpecTrail is needed.

### Manual installation

Copy the **whole** `skills/prd-author` directory, including `assets`, to one of the locations below. The source package in `skills/` does not itself configure automatic discovery. No Node.js installation is required for this route.

| Host | Project installation | Personal installation |
| --- | --- | --- |
| Codex | `.agents/skills/prd-author/` | `~/.agents/skills/prd-author/` |
| Claude Code | `.claude/skills/prd-author/` | `~/.claude/skills/prd-author/` |
| Other Agent Skills-compatible host | Use the host's documented skill directory or importer | Use the host's documented user scope |

Paths and invocation are host-specific. See [Codex skill documentation](https://developers.openai.com/codex/skills) and [Claude Code skill documentation](https://code.claude.com/docs/en/skills), checked September 10, 2026. Organization settings may affect skill availability.

### ZIP download

Download [prd-author.zip](dist/prd-author.zip).

- For Codex, Claude Code, or another filesystem-based host, extract the archive and copy the resulting `prd-author` folder to the relevant manual-install location above.
- For the Claude app, upload the ZIP through its custom skill upload flow. See [Claude's skill installation guide](https://support.claude.com/en/articles/12512180-use-skills-in-claude).

The ZIP includes both `SKILL.md` and its template. Copying only `SKILL.md` omits a required resource. To update a manual or ZIP installation, replace the previously installed folder with the new complete folder, preserving any personal edits separately.

## Usage

After installation, select `prd-author` in the host's skill picker or mention it using the host's invocation syntax. Codex CLI/IDE supports `$prd-author`; Claude Code supports `/prd-author`. Natural-language selection also depends on the host. You can also explicitly ask an agent with file access to read `skills/prd-author/SKILL.md` and apply it to your request; that exercises the instructions without testing automatic discovery.

Example requests:

- “Use prd-author to turn these notes into a concise exploratory PRD. Ask only consequential questions.”
- “Use prd-author to draft this feature request. Keep it short and leave unknown metrics explicit.”
- “Use prd-author to review this PRD for contradictions and untestable requirements. Do not rewrite it.”
- “Use prd-author to update this PRD using the attached decisions. Preserve unrelated requirements and summarize material changes.”

Markdown is the default output. Other formats use the capabilities available in the host; the skill itself does not bundle a Word renderer.

## License

[MIT](LICENSE), copyright 2026 Michael Huh. The license is also included in the skill folder and ZIP so it travels with every distribution. Referenced third-party materials retain their own terms.

## Source and validation

The package includes a copy of the [reviewed template](research/universal-prd-template.md), with repository-specific commentary removed. Keep this source and `skills/prd-author/assets/prd-template.md` synchronized when changing the template, then rebuild the archive from the skill directory. The research and review history stay outside the runtime package.

- [Research report](research/prd-research.md)
- [Independent template review](research/reviews/prd-template-review.md)
- [Independent skill review](research/reviews/prd-skill-review.md)
- [Packaging validation](research/reviews/prd-skill-validation.md)

Vercel's CLI 1.5.18 successfully discovered this skill and installed it for Codex and Claude Code in an isolated local check; both installed paths included the exact source template and instructions. The ZIP was also verified against the source. Public GitHub installation, native agent activation, and Claude app ZIP upload remain untested. Format compliance and instruction-level trials do not establish identical behavior across hosts.
