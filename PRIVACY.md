# Remote Desktop File Explorer — privacy policy

Effective **16 November 2026**. Independent developer: **AyobamiH**. Package identity: `personal-desktop-commander`. This policy concerns the URL-based, read-only **Remote Desktop File Explorer** plugin, not the separate Desktop Commander vendor service.

## What this plugin does

The plugin enables an AI client such as ChatGPT to browse ordinary files in one **explicitly authorised project folder on your own computer**. Its three tools report connectivity, list permitted folders and read bounded excerpts of permitted text files. It cannot run shell commands, edit or delete files, control the screen, access other drives arbitrarily or use the broader Desktop Commander toolkit.

## Data processed

For a requested action, the service may process the authenticated client/user identity, OAuth scopes and client registration, relative file/folder paths, filenames and types, requested line counts, and the **contents of the excerpt** you explicitly ask the tool to return. A local device agent validates the requested tool and accesses only the configured root directory; it denies hidden paths, obvious credential-like filenames, symbolic links and traversal outside that root. These restrictions are protective controls, **not a guarantee that a normal-looking file contains no sensitive material**. Configure only a project folder you are comfortable sharing with the AI host.

## How the connection works and where content goes

ChatGPT or the chosen client sends an authenticated HTTPS request to `https://reader.proofandstate.com/mcp`, hosted on **Cloudflare Workers** in the developer's Cloudflare account. OAuth registration, authorisation grants and token state are stored in the dedicated Cloudflare KV namespace used for this plugin. An owner request is forwarded over a protected Cloudflare Durable Object relay to the **outbound-only local device agent** running on the owner's computer. The agent reads the allowed file locally and sends the requested excerpt back through the Cloudflare relay to the AI client. **This makes Cloudflare an infrastructure processor of transient file content**, unlike a local-only stdio implementation. The developer does not intentionally persist the returned file text in a separate database or export it to analytics or advertisers.

Review accounts are restricted to **synthetic demonstration fixtures**, never the owner's actual files. If the owner's computer is disconnected, real file requests fail rather than being fetched from any cloud copy.

## Credentials, logs and retention

OAuth access and refresh credentials are used to authorise the MCP resource and may have the configured expiry periods (currently up to one hour for access tokens and 30 days for refresh tokens). The account's OAuth records are kept in Cloudflare KV for their functional lifetime, and can be revoked or removed in accordance with the underlying identity and platform controls. The device holds a private credential in its local protected storage; only a digest is configured as a Worker secret. The service records operational events and may expose limited request metadata in Cloudflare diagnostic/observability tooling; it is **not designed to log prompts or file excerpts**. Cloudflare and the AI client have their own operational logs and retention policies that the developer cannot unilaterally erase. The user-selected project files remain on the user's computer unless the user changes or deletes them.

AI clients such as ChatGPT process and retain submitted tool responses according to their own terms, plans and privacy settings. The developer does not sell user data or use it for targeted advertising through this plugin.

## Your control

You choose the authorised folder, control whether the local agent runs, and can disconnect the MCP plugin and stop its device agent. If connected, tool calls may be sent to the AI service; verify the selected file and content before asking to read it. You may request assistance through the [support channel](SUPPORT.md), but **never post private data or credentials in a public GitHub issue**. Deleting a chat with an AI provider is governed by that provider's controls, not by the plugin developer.

## Independent providers and changes

This is an independently developed tool, not an official product of OpenAI or the upstream Desktop Commander vendor. Cloudflare hosts the HTTPS gateway and OAuth storage; GitHub hosts the public support documents; each provider has its own policies. The developer may update this notice when data flows or capabilities materially change. It does not cover any separate Desktop Commander service or other projects.
