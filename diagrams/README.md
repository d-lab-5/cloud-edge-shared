# Diagrams

Interactive drawings of how Cloud and Edge works, made with Archify. The site
shows them in its gallery at `/diagrams/`.

- `src/<name>.<type>.json`: the source, the only file to edit.
- `<name>.html`: the page rendered from it. Never edit it by hand.
- `src/rendered.json`: which source each page was rendered from.

`npm run diagrams` renders what changed (it needs the Archify skill in
`~/.claude/skills/archify`, or `$ARCHIFY`); `npm run check` says whether every
page is in step with its source and listed once.

A diagram is listed once, with what it explains: under one of the groups
below, or in the ADR it belongs to, under that ADR's `## Diagrams`. Each line
reads `- [Title](../diagrams/<name>.html): what it explains.` and becomes the
gallery card's text.

## Overview

The whole system on one page.

- [A cloud and its edges](../diagrams/overview-cloud-and-edge.html): the parts of an edge and of the cloud it links to, who owns which file, and the three paths between them: linking, knowledge and the chat.

## Flows

What happens, in order.

- [Linking an edge to a cloud](../diagrams/flow-link-an-edge.html): the device flow, from the code the edge shows to the tenant admin's approval and the device token, with no password on the edge.
- [Syncing an A-Box both ways](../diagrams/flow-abox-sync.html): a three-way merge of statements against the last agreed version, checked by the shapes before either side is written.
- [The chat proposes, the person decides](../diagrams/flow-chat-proposal.html): Claude Code with only the edge's tools; a change it asks for waits as a proposal, runs on a click, and its outcome is told back.

## Models

What things are and how they change.

- [A connection's life](../diagrams/model-connection.html): an edge's link to one cloud, from pairing through renewal, and what 403, 410 and 426 do to it.

