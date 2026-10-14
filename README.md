# From Closed to Open: open research checklist (prototype)

**Unofficial prototype.** This is a format proposal, not a published Ulster University resource.

It is an interactive version of *From Closed to Open: Practices and Guidelines for Open Research at Ulster University*. Researchers can:

- filter actions by research stage and by what their project involves
- see which actions are expected, recommended or optional, with effort estimates
- mark each action as Yes: addressed, No: yet to be considered, Work in progress, or Not applicable (saved in their own browser)
- copy their checklist as text, or download a tailored, fillable PDF form with a status drop-down per action

## Guided adventure

`index.html` is a choose-your-own-adventure route through the same checklist. Readers pick a discipline, career stage and project scope, then move through Plan, Ethics & governance, Conduct, Publish, Share and Teach chapters. Fork questions add or remove steps, and each step has discipline and career-stage tips plus Ulster resource links. See `PLAN.md` for the design. The Ulster site blocked automated access while this was built, so **all links need a manual click-through before publishing**.

## Grant application adventure

`grants.html` is a second choose-your-own-adventure, for putting together a research grant application.

1. **Find your grant.** A search box over about 235 grants, with filters for type (fellowships, research projects, small grants, partnerships, equipment and infrastructure, international collaboration, European), funder, status (open, upcoming, closed) and a second, funder-specific filter that appears once a funder is chosen: UKRI council, NIHR programme, ERC grant type, European Commission programme, Wellcome career stage, and scheme family (fellowships, grants, prizes, chairs and so on) for Leverhulme, the British Academy, Royal Society, BHF, Cancer Research UK, the Academy of Medical Sciences and the Royal Academy of Engineering. These groups come from `CATMAP` and `CATLABEL` in the `<script>` block. "Small grants" means a project, pilot, network, travel or visit grant with a known maximum under £100,000, or a scheme that is plainly small-scale (travel awards, pump-priming, bursaries). Salary and research-leave fellowships are not counted even when they cost less than £100,000, and larger schemes that also fund small projects, such as the Nuffield Main Grants, are not tagged. Coverage: about 165 UKRI opportunities (the funding finder as of 14 October 2026, plus upcoming launches and fellowships), Leverhulme, British Academy, Wellcome, the Nuffield Foundation (each fund separately), Royal Society, Royal Academy of Engineering, Academy of Medical Sciences, NIHR programmes, Cancer Research UK, British Heart Foundation, ERC, MSCA, EIC and Horizon Europe, HSC R&D Division (Northern Ireland), Research Ireland, the Royal Society of Edinburgh, British Council, Esmée Fairbairn and the Wolfson Foundation. Each card has key facts and the funder's guidance links, and the deadline is prefilled where the call has one.
2. **Enter the deadline.** Decisions are then dated by counting back from it.
3. **Walk through the decisions.** Fork questions (partners, people or sensitive data, equipment, international work, resubmission) add decisions. Each decision has a suggested "decide by" date, the scheme's key facts and guidance links. The timeline downloads as Markdown, Word or a calendar (.ics) file.

**Grant not listed?** "Add guidance for another grant" accepts PDF, Word (.docx), text, Markdown or HTML files, or pasted text. The file is read in the browser and nothing is uploaded. A rule-based parser (no AI) pulls out the name, funder, type, award size and largest award, time commitment, eligibility, resubmission rules, page limits, dates, and which of 14 requirement types are mentioned (CV, budget, data plan, ethics, letters of support, two-stage process, interview and so on). The reader checks and edits everything before it is used. Detected requirements add decisions to the plan, and the grant is saved in the browser. Scanned (image-only) PDFs can't be read; paste the text instead.

PDF reading uses [pdf.js](https://github.com/mozilla/pdf.js) 3.11.174 (Apache-2.0, © Mozilla Foundation), vendored in `vendor/` and loaded only when a PDF is added. Serve the folder over HTTP (for example GitHub Pages) for PDF reading to work; Word, text and HTML work from a local file too.

The UKRI list is a snapshot and goes stale quickly, so each card links to its live call page. Add rows to `UKRI_ROWS` in the `<script>` block to refresh it. Scheme facts and links were gathered from the funders' own pages in October 2026. Many funder sites block automated checks, so see `LINK-CHECK.md` and click through before publishing. The week offsets are suggested planning times, not funder rules. Schemes and decisions are plain arrays at the top of the `<script>` block.

## Credits

Content: Hanna, L., Evans, E., Bond, R., Butter, S., Cahoon, A., Casey, F., McChesney, I. and Shukla, P. (2026) *From Closed to Open: Practices and Guidelines for Open Research at Ulster*. Ulster University. Licensed [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

The Expected / Recommended / Going further labels, effort estimates and "applies if" tags are draft tagging for illustration. They have not been confirmed by the Open & Responsible Research Workstream.

## Editing

The original checklist is `checklist.html` and everything for it is in that file. The checklist items are a single list near the top of the `<script>` block; the colours are set at the top of the `<style>` block.
