# Local Workspace Reader — privacy policy

Effective: **15 November 2026**. Publisher: **AyobamiH**.

## What the plugin does

Local Workspace Reader is installed and run on a computer chosen by the user. It provides three read-only MCP tools: a status check, a directory listing and a bounded excerpt from a text file inside a configured project folder. Its three review-submitted tools use Node.js filesystem APIs and a local Model Context Protocol server. A separate full Desktop Commander server is a development option in the private engineering repository but is **not** started by this review-submitted plugin. It does not include shell or file-write tools in the reviewed interface.

## Data accessed and why

When you request a file-related action, the plugin can process the **relative file or folder path**, file names and file types, requested line count, and the **text excerpt** read from the authorised folder. It uses these only to perform the requested read, return the relevant result and enforce file-size and path restrictions. The status tool returns basic feature availability, not a system inventory. It is not intended to read passwords, access tokens, payment details, health records, identity numbers or other sensitive information. Hidden files, obvious credential-like filenames, symbolic links, parent-directory traversal and some credential patterns are rejected, but filtering is not a guarantee that an ordinary-looking file contains no sensitive information. Only authorise folders and files suitable for sharing with your selected AI service.

## Where data goes and with whom it is shared

The MCP process reads the authorised file **locally**. If connected to ChatGPT or another AI host, the requested tool response and your prompts are sent to that host so it can answer you; those services have their own data-processing and retention rules. The current plugin does **not** operate a publisher-controlled cloud file store, advertising system or analytics database, and it does not intentionally send file contents to a separate developer-operated endpoint. Local operating-system or third-party dependency diagnostics may be recorded outside the plugin's control. No data is sold by the developer through this plugin.

## Retention

The plugin does not intentionally persist file contents, prompts or tool responses in a developer-run database. Transient in-memory data is released when the local process ends; source files stay on your computer until you change or delete them. If you connect an AI service, content that appears in its conversations or logs is retained according to that provider's settings and policies, **not a period the developer controls**. GitHub support issues, if you create them, remain public until edited or deleted by GitHub or their author, subject to GitHub's retention policies.

## Your choices

You can decide which project directory the plugin can access, decline a requested tool call, disconnect or uninstall the plugin and stop the local process at any time. Avoid choosing a sensitive directory. You can remove your messages from your AI host according to that provider's controls. Please do not include personal data or secrets in public support issues. For questions about the developer's implementation, use the [support page](SUPPORT.md).

## Changes and third parties

This policy covers this independently developed plugin, **not** OpenAI, GitHub, operating-system services or the upstream Desktop Commander project. We will update this page when the implementation or processing practices materially change. Review the effective date before using a new version.
