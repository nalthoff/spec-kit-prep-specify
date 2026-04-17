# Prep Specify

`Prep Specify` is a Spec Kit extension that turns rough feature ideas into clearer, paste-ready `/speckit.specify` prompts.

It is designed for the gap between "I know roughly what I want" and "I want a strong spec prompt that produces a clean first draft." The command reviews nearby repo context, asks only the highest-value clarification questions when needed, and returns text the user can paste directly into chat.

## Command

| Command | Description |
| --- | --- |
| `speckit.prep-specify.prepare` | Review a rough feature idea and synthesize paste-ready `/speckit.specify` input |

## What It Does

- Reviews the current repo before asking questions
- Uses the active Spec Kit workflow as context when available
- Supports both upstream and local Cursor layouts:
  - `.cursor/commands/speckit.specify.md`
  - `.cursor/skills/speckit-specify/SKILL.md`
- Reads `.specify/templates/spec-template.md`
- Reads `.specify/memory/constitution.md` when present
- Asks up to 5 high-leverage clarification questions
- Produces exactly one paste-ready `/speckit.specify ...` message

## Installation

### Local development install

```bash
specify extension add --dev /path/to/spec-kit-prep-specify
```

### Install from a release archive

```bash
specify extension add prep-specify --from https://github.com/<your-org>/spec-kit-prep-specify/archive/refs/tags/v1.0.0.zip
```

## Usage

In your agent:

```text
/speckit.prep-specify.prepare Add a guided onboarding flow for first-time users
```

Expected behavior:

1. Review the repo and adjacent workflow context
2. Ask only critical clarification questions if needed
3. Return a `## Paste Into Chat` section with a single `/speckit.specify ...` command

## Publishing Checklist

Before publishing this extension, update the placeholder metadata in `extension.yml`:

- Replace `repository` with your public GitHub repo URL
- Replace `homepage` with your final project or repo URL
- Update `author` if you want a different public author name

Then:

1. Push this extension to a public GitHub repository
2. Create a `v1.0.0` GitHub release
3. Test install with `specify extension add --dev ...`
4. Test install from the release ZIP URL
5. Submit a PR to the Spec Kit community catalog

Per the Spec Kit docs, this extension likely fits:

- Category: `docs`
- Effect: `Read-only`

## Community Catalog Submission Notes

To appear in the Spec Kit extension list, submit:

1. A new entry in `extensions/catalog.community.json`
2. A row in the main Spec Kit `README.md` Community Extensions table

Useful references:

- [Extension Development Guide](https://github.com/github/spec-kit/blob/main/extensions/EXTENSION-DEVELOPMENT-GUIDE.md)
- [Extension Publishing Guide](https://github.com/github/spec-kit/blob/main/extensions/EXTENSION-PUBLISHING-GUIDE.md)
- [Spec Kit Extensions README](https://github.com/github/spec-kit/blob/main/extensions/README.md)

## License

MIT
