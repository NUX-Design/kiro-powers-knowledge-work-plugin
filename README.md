# Kiro Powers Knowledge Work Plugin

Collection of domain-specific Kiro Powers stored in one repository.

Important: Kiro's `Import power from GitHub` flow expects a valid `POWER.md` in the repository root. This repository contains multiple powers in subfolders, so it is not directly installable as a single custom power from one public GitHub URL in its current layout.

## Included Powers

- `bio-research`
- `brand-voice`
- `data`
- `design`
- `engineering`
- `enterprise-search`
- `finance`
- `human-resources`
- `legal`
- `marketing`
- `operations`
- `product-management`
- `productivity`
- `small-business`

Each power folder follows the same structure:

- `POWER.md`: main power definition and usage guide
- `steering/`: task-specific steering files
- `mcp.json`: optional MCP server definitions, disabled by default

## Repo Layout

```text
<power-name>/
  POWER.md
  mcp.json
  steering/
    *.md
```

## How To Import Into Kiro

Kiro supports two relevant installation modes for custom powers:

1. `Import power from GitHub`
2. `Import power from a folder`

Because this repository has many powers and does not have a root-level `POWER.md`, the correct way to use this repository today is per-power folder import, not whole-repo GitHub URL import.

### Recommended: Import One Power From A Folder

1. Clone this repository locally.
2. In Kiro, open `Powers panel -> Add Custom Power`.
3. Select `Import power from a folder`.
4. Choose a single power directory such as `engineering`, `design`, or `product-management`.
5. Click `Install`.

The selected folder must keep this structure intact:

- `POWER.md`
- `steering/`
- `mcp.json` (optional, but included here)

### Import Multiple Powers

Repeat the folder import flow once per power you want to install.

Examples:

- import `/path/to/kiro-powers-knowledge-work-plugin/engineering`
- import `/path/to/kiro-powers-knowledge-work-plugin/design`
- import `/path/to/kiro-powers-knowledge-work-plugin/productivity`

### When GitHub URL Import Will Work

Kiro's public GitHub URL import works only when the repository root itself contains the power package, including `POWER.md`.

That means one of these structures is required:

```text
my-custom-power-repo/
  POWER.md
  mcp.json
  steering/
```

This repository is not laid out that way. Each top-level folder is a separate power package instead.

## Recommended Import Rules

- Copy the whole power folder, not only `POWER.md`.
- Do not flatten the `steering/` directory; the references inside each power expect that layout.
- Treat `mcp.json` as optional configuration. The power still works without enabling MCP servers.
- If you customize a power for your team, duplicate the folder first and edit the copy.
- If you want GitHub URL installation, publish each power as its own repository or move one power to the repository root.

## Typical Workflow

1. Pick the domain power you want.
2. Open its `POWER.md`.
3. Choose the matching workflow from the steering index.
4. Add or enable MCP servers from `mcp.json` if the workflow needs external systems.

## Example

To import the engineering power from a local clone, select this folder in Kiro:

```text
engineering/
  POWER.md
  mcp.json
  steering/
    architecture-decision-records.md
    code-review.md
    debugging.md
    deployment-checklists.md
    incident-response.md
    standup.md
    system-design.md
    technical-debt.md
    technical-documentation.md
    testing-strategy.md
```

Kiro will install that folder as one custom power.

## Notes

- This repository stores powers as normal Markdown plus JSON so they are easy to version, review, and extend.
- Kiro docs for custom power install: [Install powers](https://kiro.dev/docs/powers/installation/#from-public-github-url)
- Per the Kiro docs, the public GitHub URL flow requires `POWER.md` in the repository root.
