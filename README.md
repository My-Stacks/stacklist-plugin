# Stacklist for Grok Bot and Cursor

Stacklist is where your agent puts what it finds. Research, links and notes become **stacks** of **cards** with a one-line note on each, which your human can open on any device, share with a link, and build on later. One connection covers every bot on your account.

## Install

**Grok Bot**

- From the marketplace: open **Connect apps** in the sidebar, choose **Stacklist**, select **Add**, and finish the Stacklist sign-in in your browser.
- Or in chat: `Add this MCP server: https://stacky.stacklist.com/mcp`, then click **Authorize** on the card the bot posts.

**Cursor**

- Open the Stacklist plugin on the Cursor Marketplace and choose **Add to Cursor**. Sign in when prompted.

A free Stacklist account is enough: <https://stacklist.com/register>.

## What it does

- "Mom is visiting 31 Oct to 2 Nov. Find places to eat near us, two hotels and things to do, and put it in Stacklist." The bot researches, checks the links, and saves three stacks with a note on every card: price, area, booking tip. You open the link on your phone.
- "Pull the pricing pages for vendor A, B and C into a stack." The bot saves the pages and a short comparison. Your team opens the stack instead of scrolling the chat.
- "Keep this summary in Stacklist." The text is saved as a card in the stack you name.

Stacks created by an agent are **private** until you decide otherwise. Ask the bot to make one public and it sends you the link.

## Skills included

| Skill | When the bot uses it |
|---|---|
| `save-research-to-stacklist` | You ask it to find, collect or compare things and save them. |
| `share-a-stack-with-a-human` | You want to send a stack to someone, make it public or feature it on your profile. |
| `capture-notes-to-stacklist` | You want to keep a summary, a decision or this conversation's result. |

## Security and privacy

- Sign-in is OAuth 2.1 with PKCE. There are no API keys to paste and the plugin never asks for a password in chat.
- Tokens are held by the host's connector backend, not on the bot's machine. Disconnect from the host at any time; the token stops working.
- The plugin talks only to `stacky.stacklist.com`. Tool calls are logged for reliability; card content is processed only to provide the features you use.
- Repository contents: a manifest, the server address and three skill files. The Stacklist service itself is not part of this repository.

## For reviewers

1. Create a free account at <https://stacklist.com/register> (email code or Google).
2. Add the plugin and approve the consent screen ("Read & write your stacks, cards, profile").
3. Prompt: *"Find five unusual things to do in London this weekend and save them in Stacklist."* Expected: a reply with a stack link, a private stack with five cards, each with a one-line note.
4. Open the link while signed in at stacklist.com. The cards are there.
5. Prompt: *"Make that stack public and send me the link."* Expected: the bot asks you to confirm, then returns a link that opens in a private browser window.
6. Disconnect the plugin in the host. The next Stacklist request fails with a sign-in prompt.

## Support

engineering@stacklist.com · <https://stacklist.com>
