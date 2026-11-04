---
name: wtf
description: "WTF - Who the Fuck. Find a person at a company, show a copyable short professional brief, and optionally create a full profile using the user's named template and destination folder, including a sourced photo. Check an available workspace LinkedIn connections export for direct connections and possible introductions; skip that check when absent. Trigger on $wtf, WTF is [person] at [company], Who the Fuck is [person], or equivalent person-brief requests."
---

# WTF - Who the Fuck

Resolve a professional identity, give a short copyable brief on screen, and offer a full profile. This skill provides the workflow; it does not grant data access or guarantee provider coverage.

## Inputs and modes

- Accept a name and company, professional profile URL, or a role at a named company. Resolve identities before merging facts. For ambiguous matches, show up to three plausible candidates with distinguishing evidence and ask which one; do not build a composite person.
- Default to the short brief. If the user already requested the full profile and supplied its template and folder, complete it without asking again.
- A template name and destination folder are user-selected per request. Do not invent a permanent default, select a vaguely similar template, or let missing full-profile inputs prevent delivery of the short brief.
- Apply the host's current governing instructions and context boundaries. Keep the display name exactly **WTF - Who the Fuck**; the filesystem identifier and explicit invocation are `wtf` and `$wtf`.

## Research and identity

Discover actual tools available in this host. Use authorized native sources first, then permitted web research. Prefer employer biographies, official team pages, professional profiles, publications and dated interviews. Search broadly enough to resolve identity and current employment; research depth should fit the selected mode.

Use installed people-discovery/enrichment skills or live provider contracts where appropriate, but do not assume a Claude connector is connected in Codex or vice versa. Inspect current schemas and billing before credit-consuming work. Free/public research can proceed; paid enrichment needs the user's applicable cost authorization. Exclude Explorium/Vibe Prospecting from new workflows: the provider announced discontinuation on December 2, 2026.

Confirm the company/domain and distinguish current from former employment. Record source URLs, dates, lookup date, conflicting claims and unknown fields. Search-result snippets and provider verification labels are evidence with limitations, not independent verification. Never invent employment dates, accomplishments, contact addresses, relationships, or reporting lines. Collect professional context only; do not infer sensitive traits or pursue private personal details.

## Optional workspace connections check

Look for a LinkedIn connections export in the workspace the skill is currently operating in, including its authorized connected workspace sources. Use a known available source before rediscovering it. Do not search unrelated accounts, local histories or other workspaces to fill this gap.

If no applicable connections export is available, say **LinkedIn connections: no export available in this workspace; check skipped.** Continue the rest of the brief. If a known source cannot be read, say access was unavailable and the check was skipped. Do not ask for an export, login, browser session or new connection just to perform this optional check.

When an export is available:

1. Inspect columns and usable bounds. Search narrowly by canonical profile URL first, then name plus company/context; use name variants without merging namesakes. A common name alone is insufficient. Do not copy the whole network into an external enrichment provider.
2. Report a matching target as **Direct connection in export**, with export/snapshot date when known and connection date if present. A file's upload/modified date is not necessarily the export date; say unknown when absent. No match means **Not found in the available export**, not definitively unconnected today.
3. Identify a small number of the user's connections at the target company or with relevant professional overlap. Resolve each candidate's identity before using them. Treat export employer/title fields as historical unless refreshed from evidence.
4. Distinguish **Verified introduction path** (both user → intermediary and intermediary → target supported), **Possible introducer** (the user's connection plus relevant overlap, second edge unknown), and **Shared history only** (professional overlap, relationship unknown). A connections export usually establishes only the user's first-degree edges. Never call colleagues confirmed mutual connections or claim closeness, willingness, or an introduction is assured.
5. Cite the export and relevant rows/profile links, preserving privacy and context boundaries. Do not search private messages, email or calendars unless separately authorized. No outreach or LinkedIn actions are included.

## Optional live LinkedIn introduction-path check

Use an applicable workspace connections export first. Check available evidence for direct, second-degree and third-degree paths, without treating colleagues or shared affiliations as proof of a connection.

- **Direct:** user → target.
- **Second degree:** user → intermediary → target.
- **Third degree:** user → intermediary A → intermediary B → target.

A normal first-degree connections export cannot establish the later edges. When paths remain unknown, offer **Check live LinkedIn for introduction paths** as an optional next step. This is the exception to the no-login-request rule for the default export check: absence of an export still does not block the brief, but the user may explicitly choose live mode. Do not open or acquire an authenticated session merely because this skill was invoked.

Only after the user selects live mode, discover actual host capabilities. Use a suitable authorized native integration first. A people-search connector alone does not establish connection-graph access. Where no suitable integration can perform the check, explain the gap and use permitted signed-in browser access. Use only the user's authorized LinkedIn account/session. If login is needed, ask the user to sign in themselves through the host's supported handoff; never request credentials in chat, extract cookies or create a cloud copy of the session without explicit authorization.

Inspect the resolved target's visible connection degree and mutual-connection information. Follow only accessible, relevant links needed for a small set of possible introductions. Respect visibility restrictions; do not bypass them or bulk harvest the network.

Report **degree shown** separately from **route verified**. A 2nd/3rd-degree badge is not proof of the full chain. Mark a route verified only when every edge is supported, with source URLs, observation dates and the source's limitations. Prefer the shortest verified route; give up to three useful paths with the first person the user could approach. If only the degree is visible, say **Second/third degree shown; complete introduction route unavailable**. If access fails or no path is visible, report that exact limitation; do not infer no relationship exists.

Keep the initial short brief concise and copyable. Add degree, verified routes, candidate introducers or unknown status to its relationship section; include the full evidence chain and limitations in the named-template full profile. An optional live result can revise the short brief using the same writing-block ID. Suggest whom the user could ask, but do not message, connect, send an intro request or claim willingness to introduce.


## Short brief: copyable on screen

Aim for 150–250 words, less when evidence is sparse. Render one finished copyable artifact: in Codex use a `writing` block with variant `standard` and a unique five-digit ID; elsewhere use the host's native copyable artifact or a single clean Markdown block. Keep research commentary outside it. Include compact source links inside the brief so the copied version retains provenance.

Use this shape, adapting empty sections honestly:

**[Name] — [current role], [company]**

- **Who they are:** a concise professional summary.
- **Background:** two or three relevant career facts, expertise or public work.
- **How you may know them / introduction options:** direct-export match, up to three evidenced routes or candidate introducers, or the explicit skipped/unknown status.
- **Useful context:** one or two sourced conversation hooks; label interpretation as inference.
- **Sources / checked:** a few authoritative links, connection-export evidence if used, and lookup date.

Outside the copyable artifact, offer: **Build the full profile using your named template and destination folder.** If these were not supplied, ask for both together only when the user selects full mode. Do not withhold the short brief to collect them. Do not automatically create a file or full report from a short-brief request.

## Template and output parameters

Full-profile inputs are **person/company**, **template name or link**, and **destination folder name or link**. **Output format/file name** is optional when the template or destination convention already determines it. A portrait is included when a usable, identity-confirmed professional image is available. The short on-screen brief never requires a template or destination.

| Template supplied | Handling |
|---|---|
| Markdown (`.md`) | Use headings and fields as the structure; include a durable relative/image link if the host can save assets together. Markdown alone does not embed image bytes. |
| HTML (`.html`) | Preserve the layout and styles; embed or package the portrait durably. Suitable for a designed profile and PDF export when supported. |
| Word (`.docx`) / native Google Doc | Preserve editable document formatting and designated image placeholders using an available document tool. |
| PowerPoint (`.pptx`) / native Google Slides | Populate a profile slide or deck using an available presentation tool; preserve master, layout and image placeholders. |
| PDF (`.pdf`) | Treat as a visual/field reference. Do not promise direct editing or exact layout reproduction. Identify an available editable authoring route; explain any conversion or material fidelity limitation before proceeding. |
| Legacy Word/PowerPoint (`.doc`, `.ppt`) | Require a supported conversion route; obtain permission before changing the template's format. Do not rename an extension as conversion. |

These are candidate formats, not a guarantee that every host can render or edit them. Inspect actual document/presentation/export capabilities and the template first. If the requested input or output is unsupported, finish the short brief, state the exact gap, and offer feasible formats. Do not silently switch formats.

Preserve the supplied editable format by default. Output may be DOCX, PPTX, HTML, Markdown, a native document/presentation, or PDF **when a working renderer/exporter is available**. PDF is useful as a final viewing/sharing export; it is not the default editable source. If the user names a different output format, verify conversion support. For Markdown, report whether the photo is an image link plus saved asset, rather than claiming embedded bytes. Do not put an expiring hotlink into a supposedly self-contained file.


## Full profile: named template, named folder, photo

1. Resolve the exact template and destination folder from the user's name, ID or link in the authorized workspace. Prefer IDs after resolution. Read the complete template before drafting. If multiple plausible matches exist, ask the user to identify the intended one; do not guess. If a required template or folder is missing, keep the short brief available and request just what is missing. Creating a new destination folder requires the user's request or clear authorization.
2. Search the destination for an existing profile for this same identity. Update its confirmed master in place within the requested scope; preserve other content and the link. Do not overwrite an ambiguous match or create a duplicate. Re-read immediately before an update.
3. Follow the named template's structure, styling, format and naming convention. Fill supported fields, mark unknowns, distinguish provider data from corroborated facts, and include citations and an as-of date. Include relationship findings and their evidence/confidence in the appropriate section. If the template has no relevant place, use a concise appendix without disrupting it. No unsolicited personality or sensitive personal profiling.
4. Find a real professional portrait associated with the resolved person, preferably on an official employer bio, the person's own site, or an accessible professional profile. Establish provenance from its page context, not facial resemblance. Prefer an official downloadable headshot where available. Do not generate a replacement, identify a face from an unrelated image, bypass access restrictions, or claim image reuse rights without evidence.
5. Embed the available photo in the actual saved file, respecting aspect ratio and the template's layout, with a source-page credit/link. Use an authorized retrievable image asset and verify it rendered. An expiring remote URL alone is not a durable embedded photo. If embedding is unavailable or the identity is uncertain, state **Photo unavailable** and include the source link when useful; do not substitute someone else's picture. Missing photos do not block the profile.
6. Save in the user's named destination with its existing access controls. Use the user's requested storage service and destination; do not assume a default service. Do not silently save to a local scratch folder, create a public link, change sharing, or send it anywhere. Keep private network evidence out of any public/shared destination unless that disclosure is authorized; complete the public research portion while resolving the private-data boundary.
7. Read back the saved artifact, check the destination, name, content, citations and photo rendering where supported, and report its link plus any exact unverified item. Successful upload alone does not establish correct contents or photo rendering.

## Completion and maintenance

State what was checked versus skipped, what is still unknown, and whether a full profile was actually saved. This skill does not send messages, request introductions, invite connections, buy credits, change permissions or configure monitoring.

Keep publisher source and installed copies distinct. Do not claim automatic synchronization or installation in an unverified host.

Release 0.1.0 — Public preview. Structural validation only; live research, document rendering and relationship accuracy remain unvalidated.