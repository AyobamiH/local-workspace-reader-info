# Remote Desktop File Explorer

**Independent developer:** AyobamiH. This public repository contains the **support, privacy and terms documents only** for the Remote Desktop File Explorer plugin. It does not contain the private implementation, user data, tokens or local device executables.

The plugin connects an AI assistant to a project folder you authorise on your own PC. It can report connection status, list ordinary files and read bounded excerpts from text files using a secure HTTPS MCP endpoint at `https://reader.proofandstate.com/mcp`. A separate, authenticated outbound-only device agent reads the permitted files locally. **It does not remotely control your PC, execute terminal commands or modify files.**

This is an independent tool. It is not affiliated with OpenAI or the commercial Remote Desktop Commander service. Availability depends on the local agent, OAuth authorisation and plugin approval.

- [Privacy policy](PRIVACY.md)
- [Terms of service](TERMS.md)
- [Support and issue reporting](SUPPORT.md)

A user may decline or disconnect the plugin at any time. Do not expose secrets, private records or sensitive directories through the selected project folder.

## Read-only integration video

[See the local OAuth/MCP verification walkthrough](media/remote-desktop-file-explorer-review-demo-local-20261116.mp4). It demonstrates real local integration requests with synthetic reviewer data. **It is not a live ChatGPT production acceptance recording.** See [recording scope and limitations](media/README.md).
