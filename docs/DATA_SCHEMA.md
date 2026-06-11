# Data Schema

`data/episodes.json` is the canonical public index for this repository.

Each item represents one source video, podcast episode, lecture, or long-form talk.

## Fields

| Field | Type | Description |
| --- | --- | --- |
| `id` | string | Stable public identifier. Usually the video ID, source URL, or a title/channel fallback. |
| `video_id` | string | Source platform video ID when available. |
| `title` | string | Episode or video title. |
| `channel` | string | Channel, podcast, creator, or publisher name. |
| `published` | string | Source publish date in `YYYY-MM-DD` format when available. |
| `source_url` | string | Public source URL for verification and attribution. |
| `notion_url` | string | Empty in the public GitHub archive. Kept only for private deployments that choose to expose it. |
| `tags` | array | Topic tags produced or curated by the pipeline. |
| `rating` | number | Optional quality or importance score from the source workflow. |
| `language` | string | Detected or assigned content language. |
| `word_count` | number | Approximate word count for the main generated note. |
| `duration` | string | Human-readable duration when available. |
| `duration_seconds` | number | Duration in seconds when available. |
| `path` | string | Main deep-note Markdown path. |
| `structured_path` | string | Structured-note Markdown path when available. |
| `transcript_path` | string | Raw-transcript Markdown path when available. |

## Stability Notes

- `path`, `structured_path`, and `transcript_path` are public repository paths and can be used for links.
- `id` is intended to be stable, but early imported records may rely on fallback identifiers.
- New fields may be added over time. Existing fields should remain backward-compatible where possible.
- Private workflow fields are excluded from the public data files.
