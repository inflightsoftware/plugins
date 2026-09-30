---
name: review-feedback
description: Read the review feedback on work shared with Inflight and act on it. Use when the user asks what reviewers said, what feedback came in, what the next steps are, or wants to mark a next step done.
---

# Read and act on Inflight feedback

## Find the work

- An inflight.co link, a /p/ share or a deployed preview: call `get_feedback` with `url`.
- No link: call `get_feedback` with no arguments. It lists the user's recent versions
  with open feedback, grouped by project. Show them and ask which one, then call again
  with that version's link.

## Present it

Quote reviewers verbatim, attributed by name, with the page path each comment is on
and whether it is already addressed. Lead with the quotes; put counts last, if at all.
Threads whose `kind` is question, poll, vibe_check or ship_it are the author's own
questions to reviewers: show the prompt and the replies as answers.

Then list the version's next steps, open ones first, each with the comments it came
from, and ask which the user wants to act on.

## Close the loop

When the user says a next step is done, call `complete_next_step` with its id right
away. Do not batch completions. Never mark a step done that the user has not confirmed.

## Rules

- Do not summarize away a reviewer's words. Trim only very long comments.
- Do not delete, rename or move anything while reading feedback.
