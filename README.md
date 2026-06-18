# Kiro Powers Knowledge Work Plugin

Collection of domain-specific Kiro Powers packaged as plain folders so you can copy only the ones you need into your Kiro setup.

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

## How To Import Into Kiro Powers

This repo is organized so each top-level folder is one importable power package.

### Option 1: Import One Power

1. Choose a folder such as `engineering` or `product-management`.
2. Copy that folder into the location where you keep custom Kiro Powers.
3. Keep the folder contents intact:
   - `POWER.md`
   - `steering/`
   - `mcp.json`
4. Restart Kiro, or reload the workspace if Kiro is already open.
5. Enable or edit any MCP entries in that power's `mcp.json` only if you want external integrations.

### Option 2: Import Everything

1. Copy all top-level power folders from this repo into your Kiro Powers directory.
2. Restart Kiro or reload the workspace.
3. Turn on only the MCP servers you actually use. Every provided server is disabled by default.

## Recommended Import Rules

- Copy the whole power folder, not only `POWER.md`.
- Do not flatten the `steering/` directory; the references inside each power expect that layout.
- Treat `mcp.json` as optional configuration. The power still works without enabling MCP servers.
- If you customize a power for your team, duplicate the folder first and edit the copy.

## Typical Workflow

1. Pick the domain power you want.
2. Open its `POWER.md`.
3. Choose the matching workflow from the steering index.
4. Add or enable MCP servers from `mcp.json` if the workflow needs external systems.

## Example

To import the engineering power, copy:

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

Then reload Kiro and use the `engineering` power from your custom powers collection.

## Notes

- This repository stores powers as normal Markdown plus JSON so they are easy to version, review, and extend.
- The exact screen or menu name for loading custom powers can vary between Kiro environments. If your Kiro setup expects a specific import directory, copy the power folders there without changing their internal layout.
