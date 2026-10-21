---
name: capture-notes-to-stacklist
description: Use when the user wants to keep a summary, a decision, a draft, meeting notes or this conversation's result in Stacklist rather than a link. Saves text as a card.
---

# Capture notes to Stacklist

## Steps

1. Write the content as clean markdown with a clear title on the first line. Keep the user's words; do not pad.
2. Call `save_to_stacklist` with the markdown and, when there is one, the stack it belongs to (by name or id). Without a stack, the card lands in the user's default space and you say where.
3. For a long-form piece the user intends to publish, use `create_article` instead. It is created as a private draft; `publish_article` only when the user says so.
4. Reply with the card link the tool returned and one line on where it was filed.

## Rules

- Do not save secrets, credentials or other people's private data you came across while working.
- Do not save anything the user did not ask you to keep.
- If content was produced by an AI model, say so in the note so the human knows what they are reading.
