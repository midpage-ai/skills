---
name: legal-brief-drafter
description: "Use this skill whenever the user asks to draft, format, finalize, or review a legal brief, motion, memorandum of law, or similar court filing. Trigger on phrases like 'draft a brief', 'write a motion', 'format for [court name]', 'finalize my brief', 'court rules', 'local rules formatting', 'make this filing-ready', or any request to produce or polish a legal document intended for court submission. Also trigger when the user uploads a draft brief or memo and wants it reviewed, reformatted, or brought into compliance with court rules. This skill covers federal district courts, state courts, appellate courts (including circuit courts and state appellate courts), and specialized tribunals. If the user mentions a specific court, judge, or jurisdiction in the context of document formatting, use this skill. Do NOT use for general legal research without a drafting component, contracts, transactional documents, or non-litigation legal work."
---

# Legal Brief Drafter

Draft and format legal briefs, motions, and memoranda that comply with court-specific rules. Every court — and often individual judges — has local rules governing formatting. A filing that violates these rules can be rejected or reflect poorly on counsel. This skill ensures the agent proactively finds and applies the correct rules.

## Core Workflow

### Step 1: Identify the Court, Judge, and Filing Type

Before drafting or formatting, establish: (1) which court, (2) which judge (if known — many have individual practice rules), and (3) what type of filing (complaint, motion brief, appellate brief, memo of law, etc.). If the user hasn't specified, ask — the court identity drives everything else.

### Step 2: Find the Court Rules

**Always use web search** to find the actual rules — court rules change frequently, so do not rely on training data.

Search strategy:
1. Court's local rules — query: `[court name] local rules formatting briefs`
2. Judge's individual rules — query: `[judge name] [court] individual practice rules`
3. Fetch and read the actual rule documents from the court's website

Look for: page/word limits, font and size requirements, margin requirements, line spacing, caption format, TOC/TOA requirements, certificate of service/compliance format, signature block format, page numbering, and any structure requirements.

See `references/court-rules-guide.md` for common rule sources, typical requirements by court type, verified rules for specific courts, and formatting defaults.

### Step 3: Draft or Review the Document

The structure depends on the filing type. Getting this wrong is a common error — a complaint has a completely different structure than a motion brief.

**Complaints and Petitions** (no word/page limits in most courts):

Caption → Document title → Preliminary Statement → Parties → Jurisdiction and Venue → Statement of Facts (with subsection headings) → Causes of Action (each beginning with "Plaintiff repeats and realleges...") → Prayer for Relief (lettered subparagraphs) → Jury Demand → Signature Block

Key rules for complaints: use consecutively numbered paragraphs throughout (FRCP 10(b)); do NOT include TOC, TOA, or Certificate of Compliance; for fraud claims, plead with particularity per FRCP 9(b) (who, what, when, where, how); include the correct jurisdictional basis (diversity under § 1332 or federal question under § 1331).

**Motion Briefs / Memoranda of Law** (have word or page limits — check the rules):

Caption → TOC (if 10+ pages) → TOA → Preliminary Statement → Statement of Facts → Argument (with point headings) → Conclusion → Signature Block → Certificate of Service → Certificate of Compliance

**Table of Contents formatting:** The TOC must appear on its own page(s) — insert a page break after the last TOC entry. Include a right-aligned, underlined "Page" label at the top. Top-level sections (PRELIMINARY STATEMENT, ARGUMENT, etc.) are flush-left, bold, all-caps with dot leaders to the page number. Sub-headings under each section mirror the body's heading hierarchy (I./A./1.) with matching indents and hanging formatting. Page numbers must ALL right-align to the same position regardless of indent depth. Double-space between entries. See the TOC pattern in `references/court-rules-guide.md` for the docx-js implementation.

**Table of Authorities formatting:** The TOA must appear on its own page(s) — insert a page break after the last entry. Include a right-aligned, underlined "Page(s)" label at the top. Organize by category (Cases, Statutes, Other Authorities) with centered bold sub-headings. Each case entry uses TWO paragraphs: (1) the case name in italics ending with a comma, flush left, with no dot leader and no space after; (2) the reporter citation (not italicized) indented ~360 twips, with dot leaders to right-aligned page numbers, and double-spacing after to separate entries. Alphabetize within each category. See the TOA pattern in `references/court-rules-guide.md` for the docx-js implementation.

**Appellate Briefs** (strict word limits, specific font rules — often 14pt):

Cover Page (color-coded per circuit) → Corporate Disclosure → TOC → TOA → Jurisdictional Statement → Issues → Statement of the Case → Summary of Argument → Argument → Conclusion → Certificate of Compliance → Certificate of Service

**Reviewing/reformatting an uploaded draft:** Read the document, identify the document type, compare formatting against the court rules, flag all compliance issues, reformat while preserving substantive content, and flag any missing sections.

**Writing style:** Short sentences, active voice, strong topic sentences, well-organized point headings. Use footnotes for definitions, sourcing, and secondary points.

**Point heading formatting:** Point headings (I., II., III. and sub-headings A., B., i., ii., etc.) must be formatted as follows:
- **Single-spaced** (line spacing 240 twips / single), NOT double-spaced like body text.
- **Bold** throughout.
- **Hanging indent:** The numeral sits at the left edge of the heading's indent level, and the heading text is indented further so that wrapped lines align with the start of the text, not the numeral. This is achieved with a `hanging` indent in docx-js.
- **Indent levels:** Level 1 headings (I., II.) use a left indent of ~720 twips (0.5") with a hanging indent of ~720 twips. Level 2 headings (A., B.) increase the left indent (e.g., ~1440 twips) with a similar hanging value. Level 3 headings (i., ii.) increase further.
- **Spacing:** Use `before: 120` and `after: 240` (~6pt before, ~12pt after) so the heading has compact spacing above but more breathing room before the body text below. Do NOT use large `before` values (e.g., 240+) — this creates too much whitespace between the preceding paragraph and the heading. Do NOT use `after: 0` — this causes the heading to sit directly on top of the first body paragraph with no gap.
- **Keep with next:** Always set `keepNext: true` on point headings so they are never orphaned at the bottom of a page without at least one line of body text following them.

**Section title formatting:** Centered, bold, all-caps, underlined section titles (PRELIMINARY STATEMENT, ARGUMENT, CONCLUSION, etc.) must also set `keepNext: true` to prevent the title from appearing alone at the bottom of a page. Use `before: 120, after: 240` for consistent spacing.

See the "Point headings (hanging indent)" pattern in `references/court-rules-guide.md` for the docx-js implementation.

### Step 4: Produce the Word Document

Use the `docx` skill to create the final .docx file. Read Anthropic's public `docx` skill first: `https://raw.githubusercontent.com/anthropics/skills/main/skills/docx/SKILL.md` (repository: `https://github.com/anthropics/skills/tree/main/skills/docx`). If the environment exposes an installed local `docx` skill, prefer that local copy. Apply the formatting parameters from the court rules you found in Step 2. See `references/court-rules-guide.md` for formatting defaults when rules are silent on specific parameters, and for caption and ECF signature block conventions.

**Font selection:** Only use fonts that are universally available on Windows and Mac: Times New Roman, Arial, Georgia, Book Antiqua, Palatino Linotype. Even when a court's rules express a preference for a specific font (e.g., California prefers Century Schoolbook), use a widely available equivalent instead (e.g., Book Antiqua or Palatino Linotype for Century Schoolbook) — the rules allow "any conventional font" and a document that renders correctly everywhere is more important than a preferred-but-unavailable font that causes substitution. Use one font throughout the document; avoid mixing serif and sans-serif unless the user specifically requests it.

### Step 5: Validate and Present

Before presenting: check page/word count against court limits, verify all required sections are present, confirm formatting matches the rules.

Present with a brief summary of: which court rules you applied, any ambiguous formatting choices, any sections the user still needs to complete (attorney info, case number, specific citations), and a reminder about the Civil Cover Sheet (JS-44) for new complaints.

## Handling Edge Cases

- **Can't find specific rules:** Tell the user and apply defaults from `references/court-rules-guide.md` for that court type.
- **Judge's rules conflict with local rules:** The judge's rules typically control — flag this.
- **No court specified:** Ask before proceeding — formatting without knowing the court will likely need significant rework.
- **ECF vs. paper filing:** Most federal courts use ECF. Use `/s/` signature format for electronic filings, traditional signature lines only for paper filings. See the reference guide for details.
