# Kiro Powers Knowledge Work Plugin

Collection of domain-specific Kiro Powers.

Important: install each power only from its own public GitHub repository URL.

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

Use Kiro's GitHub installation flow for each power:

1. Open `Powers panel -> Add Custom Power`
2. Select `Import power from GitHub`
3. Paste the GitHub repository URL for the specific power
4. Click `Install`

Kiro's GitHub import requires the target repository root to contain:

- `POWER.md`
- `steering/` if used
- `mcp.json` if used

## GitHub URL Only

- Install one power per repository URL
- Do not import from a local folder
- Do not import a multi-power repository root
- Do not flatten files out of the power package

Each power should be published as its own repository with this structure:

```text
my-power-repo/
  POWER.md
  mcp.json
  steering/
```

## Recommended Import Rules

- Do not flatten the `steering/` directory; the references inside each power expect that layout.
- Treat `mcp.json` as optional configuration. The power still works without enabling MCP servers.
- Publish each power as its own GitHub repository.
- If you customize a power for your team, publish the customized version as a separate repository URL.

## Typical Workflow

1. Pick the domain power you want.
2. Open its `POWER.md`.
3. Choose the matching workflow from the steering index.
4. Add or enable MCP servers from `mcp.json` if the workflow needs external systems.

## Example

If `engineering` is published as its own repository, install it by pasting that repository URL into Kiro's `Import power from GitHub` flow.

## Notes

- This repository stores powers as normal Markdown plus JSON so they are easy to version, review, and extend.
- Kiro docs for custom power install: [Install powers](https://kiro.dev/docs/powers/installation/#from-public-github-url)
- Per the Kiro docs, the public GitHub URL flow requires `POWER.md` in the repository root of the target repository.
