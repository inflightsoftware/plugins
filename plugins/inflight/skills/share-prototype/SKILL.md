---
name: share-prototype
description: Share an HTML prototype or page with Inflight so reviewers can leave pinned comments and recordings on the rendered page. Use when the user asks for an Inflight link, to share a prototype, or to get feedback on something you built in this chat.
---

# Share a prototype with Inflight

Inflight turns an HTML file into a review link. Reviewers open it, pin comments to
elements, react, and record walkthroughs. The author reads it all back here.

## Steps

1. Take the complete HTML you are sharing. If you built it in this conversation, use
   the final version, inlined: one file, styles and scripts inside it, no references
   to local files.
2. Call `share_html` with `html` set to the full file and `file_name` to a short name
   such as `pricing-page.html`. If the user has shared an earlier version of the same
   file and you have its inflight.co/p/ link, pass it as `page` so this version joins
   that project instead of standing alone.
3. If the result has `needs_workspace`, show the listed workspaces and ask the user
   which one. Call again with `workspace` set to their choice.
4. Hand back the `url` from the result. That link is the prototype with the Inflight
   widget on it. Say who to send it to and that feedback comes back with the
   review-feedback skill.

## Rules

- Never share anything on localhost or a private network address; only HTML content
  or public links work. Say so if the user asks.
- Do not invent a workspace. Ask when the tool asks, and otherwise let the tool decide.
- Sharing creates a new version each time. Do not call `share_html` repeatedly for
  the same content.
