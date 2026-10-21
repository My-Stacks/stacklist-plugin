---
name: share-a-stack-with-a-human
description: Use when the user wants to show a stack to someone else, send a link, make a stack public, or put it on their profile. Covers the hand-over from agent to human.
---

# Share a stack with a human

## Steps

1. Find the stack with `list_stacks` or `search_stacks` and confirm it is the one the user means by name.
2. **Ask before changing visibility.** Say what public means: anyone with the link can open it, and it can be found in search and by AI systems. Only then call `update_stack` with `privacy: "public"`.
3. Optionally improve the page before sharing: `generate_summary` writes a stack description from its cards; `enrich_card_images` gives imageless cards a picture. Ask before spending AI credits.
4. If the user wants it on their profile, call `manage_featured_stacks`. Never feature a private stack.
5. Reply with the link the tool returned. The recipient needs no account.

## Rules

- A stack created by an agent stays private until a human decides otherwise.
- Do not post the link anywhere yourself (email, chat, social) unless the user asked for that specific channel.
- To undo, `update_stack` with `privacy: "private"` and `manage_featured_stacks` to unfeature.
