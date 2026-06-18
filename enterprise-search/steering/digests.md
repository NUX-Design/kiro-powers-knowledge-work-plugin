# Activity Digests

Generate daily or weekly digests across connected sources and group them by topic or project rather than by system.

## Time Windows

- `--daily`: last 24 hours
- `--weekly`: last 7 days
- custom `--since <date>` range

Default to daily when no range is provided.

## Gather Activity Across Sources

Pull recent activity from connected categories such as:

- `~~chat`: mentions, channel threads, DMs, and important discussions
- `~~email`: recent inbox threads, replies, requests, and follow-ups
- `~~cloud storage`: recently modified or shared files
- `~~project tracker`: assigned, updated, or completed tasks
- `~~CRM`: record changes or opportunity updates
- `~~knowledge base`: updated or newly created documents

## Identify Important Items

Extract and classify:

- action items
- decisions
- mentions
- updates

## Group By Topic

Merge related activity across sources under project or theme headings so the digest reflects what happened, not where it happened.

## Output Structure

```markdown
# [Daily/Weekly] Digest — [Date Range]

Sources scanned: [source list]

## Action Items
- [ ] [Action item]

## Decisions Made
- [Decision]

## [Topic or Project]
[Grouped activity summary]

## Mentions
- [Mention]

## Documents Updated
- [Document update]
```

End with summary counts for action items, decisions, mentions, and document updates.

## Failure Handling

If one or more sources are unavailable, still produce the digest and note which systems were not included.
