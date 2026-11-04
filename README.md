# WTF - Who the Fuck

Created by Chris Lockhart for **JustSignal LLC**.

Ask **WTF is [name] at [company]?** or invoke `$wtf`.

Get a copyable, sourced professional brief. Optionally create a full profile using your named template and destination, with a sourced professional photo when available. Check a connections export already in the workspace for direct connections and possible introductions; skip the check when absent. Verified paths and candidate introducers stay distinct.

## Requirements

A SKILL.md-compatible agent and authorized research tools. Full profiles require document/image tools and access to the named template and destination. No particular paid provider is required. Paid enrichment requires applicable cost authorization. No server, credentials or network data is bundled.

## Privacy

No private account IDs, Drive links, contacts or real-person dossiers are included. No messages, introductions, connection requests, credit purchases or permission changes are performed. No sensitive personal profiling. A photo's availability does not establish reuse rights.

## Status and distribution

Version 0.1.1 public preview. Structural validation only; live research, document rendering and relationship accuracy remain unvalidated. The same skill is packaged for portable plugin and Claude plugin distribution. Connector authorization depends on the host. Directory approval is not claimed.

## License

MIT License. Copyright (c) 2026 JustSignal LLC. See LICENSE for the complete terms.

## Inputs and outputs

**Short brief:** person and company (or a professional profile URL); output is a copyable, sourced on-screen brief. No template or folder needed.

**Full profile:** name/link of your template and destination folder. Output format and filename are optional if established by your template. A sourced professional photo is included when available; otherwise the profile says Photo unavailable.

**Optional network check:** uses a LinkedIn connections export already available in the current workspace. If absent or inaccessible, it says so and skips the check. It does not require a login or export upload. Possible introducers are not claimed as verified mutual connections.

| Template | Handling |
|---|---|
| Markdown | Structured headings and fields; photo linked with a saved asset when supported |
| HTML | Designed profile; durable image embedding or packaged assets |
| DOCX / Google Docs | Editable document, subject to connected document tools |
| PPTX / Google Slides | Editable slide/deck, subject to connected presentation tools |
| PDF | Visual/field reference; direct editing and exact reproduction are not guaranteed |
| DOC / PPT | Supported conversion required; no silent format change |

Preserve the editable format by default. PDF can be a final export when a renderer is available. The skill checks actual host capabilities before promising a format.

## Optional live LinkedIn mode

After export-based checks, you may choose **Check live LinkedIn for introduction paths**. The skill then uses an authorized integration or permitted authenticated browser session, asking you to sign in yourself if needed. This is optional; no session is requested automatically for the initial brief. It checks visible second/third-degree relationships and introduction chains. A degree badge is reported separately from a verified route; every link needs evidence. Restricted or unavailable paths remain unknown. No messages, connection requests or introduction requests are sent.

## Data flows

The skill may send the target name, company or professional profile URL to user-authorized research/search/enrichment providers. It may read a workspace connections export and, only when selected, visible relationship information through an authenticated LinkedIn session. A requested full profile is saved to the user's named destination. No publisher-operated backend receives or retains this data. Host, storage, research-provider and LinkedIn policies govern their own processing and retention.

[Privacy notice](PRIVACY.md)
