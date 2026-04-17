# Community Submission Template

Use this file when you are ready to submit `prep-specify` to the Spec Kit community catalog.

## Catalog Entry

Add an entry like this to `extensions/catalog.community.json` in the Spec Kit repository:

```json
{
  "prep-specify": {
    "name": "Prep Specify",
    "id": "prep-specify",
    "description": "Clarify rough feature ideas into paste-ready /speckit.specify prompts",
    "author": "Nick",
    "version": "1.0.0",
    "download_url": "https://github.com/<your-org>/spec-kit-prep-specify/archive/refs/tags/v1.0.0.zip",
    "repository": "https://github.com/<your-org>/spec-kit-prep-specify",
    "homepage": "https://github.com/<your-org>/spec-kit-prep-specify",
    "documentation": "https://github.com/<your-org>/spec-kit-prep-specify/blob/main/README.md",
    "changelog": "https://github.com/<your-org>/spec-kit-prep-specify/blob/main/CHANGELOG.md",
    "license": "MIT",
    "requires": {
      "speckit_version": ">=0.2.0"
    },
    "provides": {
      "commands": 1,
      "hooks": 0
    },
    "tags": [
      "docs",
      "process",
      "specification",
      "prompt-prep"
    ],
    "verified": false,
    "downloads": 0,
    "stars": 0,
    "created_at": "<replace-with-iso-timestamp>",
    "updated_at": "<replace-with-iso-timestamp>"
  }
}
```

## README Table Row

Add a row like this to the Community Extensions table in the main Spec Kit `README.md`:

```markdown
| Prep Specify | Clarifies rough ideas into paste-ready `/speckit.specify` prompts | `docs` | Read-only | [spec-kit-prep-specify](https://github.com/<your-org>/spec-kit-prep-specify) |
```

## Before You Submit

- Replace every `<your-org>` placeholder
- Create the public GitHub repository
- Tag and publish release `v1.0.0`
- Confirm the ZIP download URL works
- Test `specify extension add prep-specify --from <release-url>`
