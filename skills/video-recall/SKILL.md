---
name: video-recall
description: Find a video the user watched or answer a question about one. Use when the user says "there was a video about…", "where did I see…", "what did that video say about…", or asks about a YouTube link.
---

The user's watch history is searchable through the `watch_find` and `watch_ask` tools. It covers
every video they watched, including ones they didn't save, with full transcripts.

1. To find a video, call `watch_find` with the idea in the user's own words. Try a second phrasing
   (names, product terms, a quote) if the first misses. Use the date if the user gives one
   ("yesterday", "last week") to choose between hits.
2. Reply with the title, the channel, the timestamped link and one line on why it matches. If two
   or three candidates are close, list them and ask which one.
3. To answer a question about one video, call `watch_ask` with the URL or id and the question.
   Quote its `[mm:ss]` timestamps so the user can jump to the moment.
4. Don't summarise a transcript yourself from memory; use `watch_ask`.

The tools only see what was said (transcripts), not what was on screen. Say so if the question is
about visuals.
