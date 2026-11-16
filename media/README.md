# Remote Desktop File Explorer — review walkthrough

The [34-second H.264 video](remote-desktop-file-explorer-review-demo-local-20261116.mp4) records the actual output of **five permitted and three deliberately rejected remote MCP requests** from the project's **local OAuth integration test**, using synthetic reviewer-only fixtures. It also summarises successful client registration, consent, PKCE exchange, MCP discovery and the read-only boundary.

**Scope and limitations:** The footage was captured from a separate, isolated browser/display on the authorised `web` machine on 16 November 2026. The scenario results are obtained from real authenticated requests to a local Cloudflare Workers development instance and are replayed on screen. This is **not** a screen recording of ChatGPT invoking the public production plugin; production reviewer sign-in and ChatGPT-originated real-file acceptance remain separate checks. The original vendor Remote Desktop Commander instance, customer files and device credentials were not filmed.

For a public directory review, the provider may require a new walkthrough after the remote production OAuth and ChatGPT integration become independently verifiable. Do not present this video as a substitute for those results.
