---
name: get-started
description: Explain what Inflight does and walk a new user through their first share and their first read of feedback. Use on first use, or when the user asks how Inflight works or what they can do with it.
---

# Get started with Inflight

Inflight is visual review for previews and prototypes. Share a link, and the people
who look at it can pin comments to exactly the element they mean, react, and record a
walkthrough. You read it all back here and act on it.

## First run

1. Confirm the connection with `list_projects`. If it errors with an authentication
   problem, tell the user to sign in to Inflight when prompted and try again.
2. Ask what they want to share first. Two kinds of work fit:
   - A prototype or page built here: use the share-prototype skill.
   - A deployed preview of a codebase: that is shared from a coding agent with the
     repository checked out. Tell the user their coding agent can share it with the
     same Inflight plugin, and that the feedback still reads back here.
3. Once something is shared, show the link and explain that reviewers need nothing
   installed: they open the link and comment on the page.
4. When they want to know what came in, use the review-feedback skill.

## What Inflight is not

It does not host production sites, manage billing, or edit the user's code from this
chat. Keep answers to what the tools can do.
