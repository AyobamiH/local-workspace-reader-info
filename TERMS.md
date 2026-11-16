# Remote Desktop File Explorer — terms of service

Effective **16 November 2026**. Publisher: **AyobamiH**.

**Remote Desktop File Explorer** is a read-only AI plugin designed to browse and read selected project files from a computer that the user operates and authorises. Its authenticated HTTPS endpoint is `https://reader.proofandstate.com/mcp`. The initial release offers only connection status, directory listing and bounded text-file reading; it does **not** grant shell commands, filesystem modification, unattended desktop control or screen sharing.

## Authorised use

You must have the lawful right to access every file and folder you authorise this plugin to read, and you must comply with your workplace, AI service and operating-system policies. Do not configure the tool to access other people's data without permission, credentials, protected records or sensitive content you would not knowingly share with your AI provider. The owner must keep their local device credential secret and should select the minimum necessary folder.

## Account access and availability

The HTTPS service uses OAuth authorisation and a separate local device identity. The developer may disable sessions, revoke abusive or compromised authorisation, or change access controls to protect users and infrastructure. If your computer or the outbound local agent is offline, the plugin cannot retrieve actual files. A synthetic reviewer environment is not connected to any real user's computer.

## What the tool does not guarantee

The service is provided **as is** to the extent permitted by applicable law. No filtering mechanism can guarantee that a file contains no private data; no remote network or cloud dependency has guaranteed availability. Verify outputs, retain your important data and avoid placing sensitive information in the authorised root. Nothing in these terms removes consumer rights or legal liabilities that cannot lawfully be excluded.

## Third-party technology

The project is independently developed and does not claim endorsement by OpenAI, Cloudflare or the Desktop Commander maintainers. The upstream Desktop Commander toolkit is maintained and tested separately and is **not** the remote read-only feature exposed in this plugin. Use of ChatGPT or other AI clients, Cloudflare or GitHub is subject to those providers' applicable terms and policies.

## Support

See [support](SUPPORT.md) and the [privacy policy](PRIVACY.md). Do not send passwords or confidential files in public issue reports.
