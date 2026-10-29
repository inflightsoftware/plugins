# Inflight

Visual review for previews and prototypes. Share a link, let reviewers pin comments
and record walkthroughs on the live page, and read the feedback back in chat.

## What it does

- **Share work for review.** `share_html` turns an HTML prototype into an inflight.co
  link; `share_app` uploads a built web app; `share_preview` binds a deployed preview.
  Reviewers open the link and comment on the page — nothing to install on their side.
- **Read feedback back.** `get_feedback` quotes each reviewer verbatim with the page
  path and whether the comment is addressed, then lists the next steps derived from
  the discussion. `complete_next_step` marks one done once you have addressed it.
- **Organize.** List, rename, file and delete projects and folders in your workspace.

## Setup

In Claude Code:

```
/plugin install inflight --marketplace inflightsoftware/plugins
```

The plugin connects to the hosted Inflight MCP server at `https://mcp.inflight.co/mcp`.
On first use your agent opens a browser sign-in; approve it with your Inflight account
(create one free at [inflight.co](https://inflight.co)).

Skills included:

- `get-started` — first share and first read of feedback
- `share-prototype` — share an HTML prototype for review
- `review-feedback` — read and act on reviewer feedback

## Example prompts

- "Share this prototype with Inflight for review"
- "What feedback came in on my Inflight previews?"
- "Implement the feedback that came in on my Inflight prototype"

## Privacy Policy

The plugin sends the content you choose to share (HTML, app builds, preview URLs) and
your requests for feedback to Inflight's servers, authenticated with your Inflight
account. Inflight stores shared work and feedback to provide the service and does not
sell it. Full policy, including retention and third-party processors:
[inflight.co/privacy](https://inflight.co/privacy).

## Support

[inflight.co/support](https://inflight.co/support) · support@inflight.co

## License

MIT
