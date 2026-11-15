---
name: kb-first
description: Look things up in the user's knowledge base before answering. Use for any question about the user's homelab, servers, services, network, backups, projects, past decisions, or "what's the state of X" — anything where the user's own notes beat general knowledge.
---

The user keeps a personal knowledge base (KB) of notes on their infrastructure, projects and
decisions. It is reachable through the `aikb_search` and `aikb_read` tools. It is the source of
truth for anything about the user's own setup; your general knowledge is not.

1. Search first. Call `aikb_search` with the question in plain words (for example
   "what is currently broken?", "how are backups done for X?"). Run two or three searches with
   different wording when the first misses.
2. Read before you rely on a hit. Open the most relevant files with `aikb_read`. Search results
   are excerpts and can be out of context.
3. Check dates. Notes carry a `Last Updated` line or `last_updated` front matter. Say how old the
   information is when it is more than a couple of weeks old, and treat it as possibly stale.
4. Answer with sources. Name the file path(s) you used. Separate what the notes say from what you
   are inferring.
5. Say when the KB has nothing. Do not fill the gap with a guess about the user's setup. Offer
   general guidance and label it as general.
6. Never repeat credentials. If a note contains a password, token or key, do not quote it; say
   where it is stored instead.

The KB tools are read-only. If the user asks you to record something, draft the note text in your
reply so they can add it themselves.
