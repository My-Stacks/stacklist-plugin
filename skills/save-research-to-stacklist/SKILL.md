---
name: save-research-to-stacklist
description: Use when the user asks you to find, collect, compare or research things and save them "in Stacklist", or to save links for later. Turns research into one stack of cards with a one-line note on each.
---

# Save research to Stacklist

A stack is a named, ordered set of cards. A card is a saved link with a title, a note, tags and an image. Your human opens the stack on any device; no app needed.

## Steps

1. **Check for an existing stack first.** Call `list_stacks` (or `search_stacks` with a keyword). If a stack for this topic already exists, add to it instead of creating a second one.
2. **Validate the links** with `validate_urls` before saving. Drop dead or redirecting links; do not save a link you have not opened.
3. **Create the stack** with `create_stack`. Name it specifically and front-load the subject, 30 to 48 characters ("London 5-8 Nov: fun things to try", not "London list"). Write stack notes of 70 to 160 characters saying what is inside and for whom. Set a category. Leave it **private** unless the user asked for public.
4. **Add the cards** with `add_cards`. Pass the URL and, for every card, a one-line `notes` value with the facts the human will decide on: price, area, timing, booking tip, caveat. Title and image are extracted automatically; override the title only when the extracted one is unclear. Send cards in batches of up to 10.
5. **Tag** with `auto_tag_cards` once the cards are in, or pass 3 to 6 consistent tags yourself.
6. **Reply with the link** the tool returned and a short list of what you saved. Do not construct URLs by hand.

## Rules

- One topic, one stack. Several topics, several stacks (Restaurants, Hotels, Things to do), named so they sort together.
- Never make a stack public, feature it on a profile or publish anything without the user asking. Private is the default and the safe choice.
- If a save fails, say so plainly and name what was not saved. Do not report success for cards that returned an error.
- Do not ask for passwords or API keys. Sign-in happens through the host's connect flow.
