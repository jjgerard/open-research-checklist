# Plan: "Choose your own open research adventure"

The adventure is the site home page, `index.html`. The original flat checklist is kept as `checklist.html` and linked from it.

## Flow
1. **Choose your character**: discipline, career stage, project scope, then an optional "my project involves" multi-select (human participants, code, external funding, partners, Indigenous data, teaching).
2. **The journey**: chapters Plan, Ethics & governance, Conduct, Publish, Share data & code, Teach. Each chapter is a sequence of scenes.
   - Fork scenes ask a yes/no/not-sure question (e.g. "Will you work with people or personal data?"). The answer adds or removes the scenes that follow, so the path differs per person.
   - Action scenes carry: what to do, why, a tip for the chosen discipline and career stage, effort, Expected/Recommended/Going further label, and resource links.
   - Each action: Done / Later / Not for me. Back, Next, a chapter map and progress bar are always visible.
3. **Your map**: summary checklist (done / to do later), copy as text, print. State is saved in `localStorage`.

## Content and links
- Content is based on the checklist items already in `checklist.html` (From Closed to Open, CC BY 4.0).
- Links go to Ulster pages: Open research hub, Research hub, Governance & ethics (ethics, research governance, GDPR), RDM, Pure, Library OA guides.
- Only URLs already used in the prototype, plus the three the brief gave, are used. The Ulster site returned 403 to my tooling, so **links are unverified** and need a manual click-through before publishing.
- Labels and tags are draft tagging, not confirmed by the workstream (same caveat as the prototype).

## Implementation
Single self-contained HTML file (no build step, no external scripts), mobile-first, keyboard accessible, light/dark, same palette as `checklist.html`. Data-driven: scenes live in one array; `when(profile)` decides inclusion.

## Steps
1. Write plan (this file). 2. Build the adventure. 3. Test in Chromium with Playwright (paths for several profiles, phone width). 4. Make the adventure `index.html`, keep the original as `checklist.html`, update README, commit and push.
