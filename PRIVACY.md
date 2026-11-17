# Proof & State Desktop — privacy policy

Effective **17 November 2026**. Independent developer: **AyobamiH**. Package identity: `remote-desktop-file-explorer`, previously displayed as Remote Desktop File Explorer. This policy does not cover the separate commercial Desktop Commander service.

## Capabilities and information processed

The owner connects explicitly enrolled workspaces to an authenticated MCP gateway. Operations may include file listings, bounded file contents and searches, proposed file edits, PDF generation, isolated Linux commands and durable jobs. Native Windows enrollment currently supports read-only operations. Screen control and general outbound networking are not provided.

Requests and responses can contain device identifiers, relative paths, filenames, file excerpts, proposed new content, command arguments, process/job identifiers, output, errors, approval request IDs and operation receipts. These may be sensitive even when a filename looks ordinary. Enrol only workspaces you intend to share with the AI client. Hidden, credential-like, parent and symlink paths are restricted; this is not a guarantee that ordinary files contain no private material.

## Infrastructure and transmission

The HTTPS endpoint `https://reader.proofandstate.com/mcp` is hosted on Cloudflare Workers. OAuth client registrations, grants and token state are stored in the dedicated Cloudflare KV namespace. A Durable Object routes authenticated calls over an outbound WebSocket to the selected device agent. Requested content and results travel through Cloudflare to the AI client. Cloudflare therefore processes transient content; this is not a local-only connection.

The developer does not intentionally export file contents to advertising or analytics services or sell user data. Operational events may be recorded in Cloudflare observability; the application is not designed to log credentials or file excerpts. Cloudflare and the AI provider have their own logs, retention rules and privacy settings.

## Approvals and local records

Owner write and execution operations require the corresponding OAuth scopes and a device-local exact one-use approval. The agent keeps pending requests, consumed approvals, bounded results and job records on the owner machine to prevent replay and support recovery. These records can include proposed file content, commands and output. They are not automatically erased when a chat is deleted or an OAuth token is revoked. Local access is restricted to the owner account; the owner controls retention and removal. Removing recovery records may impair replay protection and must be handled deliberately.

## Reviewer and browser demo

Reviewer credentials are distinct from owner credentials. The full-capability review demo, when enabled, routes exclusively to a dedicated synthetic workspace. It uses the same execution code with separate device authentication, bounded resources and demo-only exact approvals. It cannot select owner devices or read their operation receipts. Demo filesystem changes, output and receipts are RAM-backed and reset on host reboot; they are not durable personal storage. Do not put personal information, credentials or confidential material in the shared review fixture.

The browser demo uses OAuth with PKCE. Temporary login transaction information is stored in that browser tab's session storage until exchanged or restarted. The resulting access token is held in page memory, and disconnect requests revocation. Closing the page clears its memory but does not itself guarantee server-side revocation. Access tokens have a bounded lifetime.

## Credentials and user control

Access tokens currently last up to one hour; refresh tokens may last up to 30 days. OAuth state remains in Cloudflare for its functional lifetime and can be revoked or removed through the applicable controls. Device credentials are stored in protected local files; their digests are configured on the Worker. Never share owner or reviewer codes in chat, public issues or recordings.

The owner chooses enrolled devices and workspaces, approves effects, stops agents and disconnects the plugin. Revocation prevents future authorised access but does not undo completed writes or commands, delete local receipts or erase AI-provider copies. Cancellation can leave partial effects. Ask the AI provider about its copies and settings; contact the developer through [support](SUPPORT.md) for product assistance without posting private data.

This is independent software, not an official OpenAI, Cloudflare or Desktop Commander product. GitHub hosts these public policy and support documents. Material changes to capabilities or data flows will be reflected in this notice.
