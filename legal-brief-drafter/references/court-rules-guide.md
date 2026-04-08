# Court Rules Reference Guide

A quick reference for locating court-specific formatting rules. Read this when you need help finding rules for a particular jurisdiction.

## Federal Courts

### U.S. District Courts (Trial Level)

**Where to find rules:**
- Each district has its own website: `[district abbreviation].uscourts.gov` (e.g., `nysd.uscourts.gov` for S.D.N.Y.)
- Look for "Local Rules" or "Rules & Procedures" in the navigation
- Individual judge rules are usually under "Judges" → [Judge Name] → "Individual Practices" or "Part Rules"
- Search query: `[district name] local civil rules` or `[judge name] individual rules [district]`

**Typical requirements:**
- Governed by Federal Rules of Civil Procedure (FRCP) + local rules
- Margins: 1 inch on all sides
- Font: varies by district — many require 12pt proportional font (Times New Roman or similar)
- Line spacing: double-spaced body text
- Page limits: typically 25 pages for opening/opposition briefs, 10-15 pages for replies (but varies significantly)
- ECF filing is standard; most require PDF uploads

**Notable districts with strict formatting:**
- S.D.N.Y.: Individual judge practices vary widely; always check the specific judge
- N.D. Cal.: Has specific word limits rather than page limits for many motions
- E.D. Tex.: Known for detailed individual judge requirements, especially in patent cases
- D. Del.: Detailed formatting rules for patent and corporate litigation

### U.S. Courts of Appeals (Circuit Courts)

**Where to find rules:**
- Each circuit: `ca[number].uscourts.gov` (e.g., `ca2.uscourts.gov` for Second Circuit)
- Governed by Federal Rules of Appellate Procedure (FRAP) + circuit rules
- Search query: `[circuit] court of appeals brief formatting rules`

**Typical requirements (per FRAP):**
- Word limits (not page limits): 13,000 words for principal briefs, 6,500 for reply briefs
- Certificate of compliance with word count is required
- Font: 14-point proportional font OR 12-point monospaced
- FRAP 32 specifies: Century Schoolbook, Times New Roman, or similar serif font at 14pt
- Margins: at least 1 inch on all sides
- Cover page with specific color coding (blue for appellant, red for appellee, etc. — varies by circuit)
- Table of Contents and Table of Authorities required
- Some circuits (e.g., Seventh Circuit) have very specific typography requirements

**Circuit-specific notes:**
- 7th Circuit: Judge Posner's legacy — strong preference for clear, readable typography; specific font guidance
- 9th Circuit: Requires electronic filing and has specific PDF bookmarking requirements
- D.C. Circuit: Additional requirements for cases involving agency review
- Federal Circuit: Specialized rules for patent and trade cases

### U.S. Supreme Court

- Rules available at `supremecourt.gov`
- Very specific formatting: booklet format (6⅛ x 9¼ inches), Century Schoolbook 12pt
- Word limits: 13,000 for merits briefs
- Rarely relevant for this skill, but included for completeness

## State Courts

### State Trial Courts

**Where to find rules:**
- Search: `[state] [court name] local rules` or `[state] rules of civil procedure`
- Many states publish rules through their judiciary website: `courts.[state].gov` or `[state]courts.gov`
- County-level courts may have additional local rules

**Common patterns:**
- Many states model rules on FRCP but with local variations
- Page limits vary widely (some states have no specific limits for trial-level briefs)
- Font and margin requirements are often less prescriptive than federal courts
- Some states still require paper filing in addition to electronic

**Notable state courts:**
- New York Supreme Court: Has specific Commercial Division rules with detailed formatting requirements; individual judges (Parts) have their own rules
- California Superior Court: Rules vary significantly by county; LA County, SF County, and Santa Clara County each have distinct local rules
- Texas District Courts: Individual judge preferences are important; check the judge's website
- Delaware Chancery Court: Specific rules for corporate litigation, very detailed formatting

### State Appellate Courts

**Where to find rules:**
- Search: `[state] court of appeals brief format rules` or `[state] appellate rules`
- Most states have appellate rules similar to FRAP but with state-specific variations

**Common requirements:**
- Word or page limits (varies by state)
- Table of Contents and Table of Authorities
- Certificate of Compliance
- Specific cover page requirements
- Some states require specific paper size or binding (increasingly rare)

## Specialized Courts

- **Bankruptcy Courts**: Follow federal local rules + bankruptcy-specific rules; search `[district] bankruptcy local rules`
- **Tax Court**: Has its own set of rules at `ustaxcourt.gov`
- **Court of Federal Claims**: Rules at `uscfc.uscourts.gov`
- **Immigration Courts**: EOIR rules, though less relevant for traditional brief formatting

## Common Formatting Defaults

When you cannot find specific rules, these are safe defaults for US courts:

| Element | Default |
|---------|---------|
| Paper size | US Letter (8.5 x 11 inches) |
| Margins | 1 inch all sides |
| Body font | Times New Roman 12pt (trial) or 14pt (appellate). For California appellate courts, use Book Antiqua or Palatino Linotype 13pt (widely available equivalents to the preferred Century Schoolbook) |
| Line spacing | Double-spaced body text |
| Block quotes | Single-spaced, indented 0.5 inches both sides |
| Footnotes | Single-spaced, 10pt |
| Page numbers | Centered at bottom |
| Citation format | Bluebook |

These defaults are a reasonable starting point but should always be verified against the actual court rules. Tell the user whenever you're falling back to defaults.

## Verified Court Rules (from test runs)

These rules have been verified against actual court documents. Use them as a starting point but always re-verify with a web search, as rules change.

### S.D.N.Y. (Southern District of New York) — as of January 2, 2025

Source: Joint Local Rules, S.D.N.Y. and E.D.N.Y., effective January 2, 2025 (Local Civil Rule 7.1)

- Font: 12-point type or larger (10-point for footnotes)
- Margins: at least 1 inch on all sides
- Spacing: double-spaced body text; headings, footnotes, and block quotations may be single-spaced
- Motion brief word limits: 8,750 words for opening/opposition briefs; 3,500 words for replies (does not include caption, TOC, TOA, signature blocks, or certificates)
- Memoranda of 10+ pages must include a table of contents and table of authorities
- All memoranda must include a certificate of word-count compliance
- Individual judges often have their own rules that may modify these defaults — always check
- ECF filing is standard; `/s/` signature format expected
- Complaints have no word or page limit but must comply with the same font, margin, and spacing rules

## Caption Formatting (Federal Courts)

The caption is the header block identifying the court, parties, and case number:

- Court name centered and bold at the top (e.g., "UNITED STATES DISTRICT COURT / SOUTHERN DISTRICT OF NEW YORK")
- Plaintiff name(s) bold, left-aligned, with "Plaintiff," in italics below
- "v." centered, with the case number right-aligned on the same line (use tab stops)
- Defendant name(s) bold, left-aligned, with "Defendant." in italics below
- A horizontal rule below the caption block to separate it from the document body
- For new filings: "Civil Action No. __________"

## ECF (Electronic Case Filing) Conventions

Most federal courts use ECF. Key conventions that affect document formatting:

- Signature blocks use `/s/ [Attorney Name]` format, not a physical signature line
- Documents are filed as PDFs (the court system stamps a header with case number, document number, filing date, and page count)
- The court-stamped header appears at the top of every page — do not try to replicate this in the document; the ECF system adds it automatically
- File names should be descriptive (e.g., "Complaint.pdf", "Memorandum-in-Support-of-MTD.pdf")
- A Civil Cover Sheet (JS-44 or local variant) must accompany new complaints

## docx-js Patterns for Legal Documents

Short snippets for common legal document layouts. Use with `const { Paragraph, TextRun, TabStopType, TabStopPosition, AlignmentType, BorderStyle } = require("docx");`

**Table of Contents (TOC):**

The TOC must be on its own page(s). Insert a page break after the last TOC entry before the body begins.

Layout rules:
- Right-align "Page" (underlined) on the first line of the TOC, before any entries.
- Top-level section titles (PRELIMINARY STATEMENT, RELEVANT FACTS, LEGAL STANDARD, ARGUMENT, CONCLUSION) are flush-left, all-caps, bold, with dot leaders to a right-aligned page number. Space between top-level entries should be generous (double-spaced, `after: 200`–`240`).
- Sub-headings under RELEVANT FACTS and ARGUMENT use hanging indents identical to the body point headings (I./A./1. pattern), with dot leaders to the page number. The page number must ALWAYS be right-aligned to the same position (9360 twips) regardless of indent level.
- Sub-heading TOC entries should also be double-spaced from each other (`after: 200`).
- For long headings that wrap, the dot leader and page number appear only on the last line.

```js
// CRITICAL: The tab stop position must ALWAYS be 9360 (the right margin),
// NOT 9360 - indent. Using 9360 - indent was a previous bug that caused
// page numbers on indented entries to drift left instead of staying
// right-aligned.
//
// The "Page" header line:
// new Paragraph({
//   alignment: AlignmentType.RIGHT,
//   spacing: { after: 120 },
//   children: [new TextRun({ text: "Page", font: FONT, size: SZ, underline: {} })],
// })

function tocEntry(text, page, indent = 0, { bold = false, allCaps = false } = {}) {
  return new Paragraph({
    spacing: { line: 240, after: 200 },
    indent: { left: indent },
    tabStops: [{ type: TabStopType.RIGHT, position: 9360, leader: "dot" }],
    children: [
      new TextRun({ text, font: FONT, size: SZ, bold, allCaps }),
      new TextRun({ text: `\t${page}`, font: FONT, size: SZ }),
    ],
  });
}

// Top-level sections (flush left, bold, all-caps):
// tocEntry("PRELIMINARY STATEMENT", "1", 0, { bold: true, allCaps: true })
// tocEntry("RELEVANT FACTS", "4", 0, { bold: true, allCaps: true })
//
// Sub-headings use hanging indents. For TOC, combine numeral + text into one
// string and use the same indent levels as the body point headings:
// Level 1 (I., II.):   indent 720
// Level 2 (A., B.):    indent 1440
// Level 3 (1., 2.):    indent 2160
//
// tocEntry("I.    Plaintiffs have partnered with restaurants...", "4", 720)
// tocEntry("A.   The Tipping Law compels speech...", "9", 1440)
// tocEntry("1.   The Tipping Law triggers strict scrutiny.", "12", 2160)
//
// IMPORTANT: Use plain spaces (not \t) between numeral and title text.
// The only \t should be before the page number — it triggers the dot leader.
//
// After the last TOC entry, insert a page break:
// new Paragraph({ children: [new PageBreak()] })
```

**Table of Authorities (TOA):**

The TOA must be on its own page(s). Insert a page break after the last entry.

Layout rules:
- Title: "TABLE OF AUTHORITIES" centered, bold, all-caps.
- Right-align "Page(s)" (underlined) below the title.
- Category sub-headings ("Cases", "Statutes", "Other Authorities") are centered and bold.
- Each case entry is TWO paragraphs (this is critical for proper formatting):
  - **Line 1 (case name):** The full case name in italics, ending with a comma. No dot leader. Flush left. Minimal spacing after (`after: 0`). Single-spaced (`line: 240`).
  - **Line 2 (reporter cite + pages):** The reporter citation, court, and year — NOT italicized — indented ~360 twips, with a dot leader tab stop at 9360 to a right-aligned list of page numbers. Double-space after this line (`after: 200`) to separate from the next entry.
- Statutes and other authorities follow the same two-line pattern but without italics on line 1 (or use italics only for the title portion if applicable).
- Alphabetize entries within each category.

```js
// "Page(s)" header:
// new Paragraph({
//   alignment: AlignmentType.RIGHT,
//   spacing: { after: 120 },
//   children: [new TextRun({ text: "Page(s)", font: FONT, size: SZ, underline: {} })],
// })
//
// Category heading (e.g., "Cases"):
// new Paragraph({
//   alignment: AlignmentType.CENTER,
//   spacing: { before: 240, after: 200 },
//   children: [new TextRun({ text: "Cases", font: FONT, size: SZ, bold: true })],
// })

// Each case = two paragraphs:
function toaCaseName(name) {
  // Line 1: italic case name ending with comma, flush left, no dot leader
  return new Paragraph({
    spacing: { line: 240, after: 0 },
    children: [
      new TextRun({ text: name, font: FONT, size: SZ, italics: true }),
    ],
  });
}

function toaCiteLine(citation, pages) {
  // Line 2: reporter cite indented, dot leader to right-aligned page numbers
  return new Paragraph({
    spacing: { line: 240, after: 200 },
    indent: { left: 360 },
    tabStops: [{ type: TabStopType.RIGHT, position: 9360, leader: "dot" }],
    children: [
      new TextRun({ text: citation, font: FONT, size: SZ }),
      new TextRun({ text: `\t${pages}`, font: FONT, size: SZ }),
    ],
  });
}

// Usage — each case produces two paragraphs:
// toaCaseName("44 Liquormart, Inc. v. Rhode Island,")
// toaCiteLine("517 U.S. 484 (1996)", "15, 16")
//
// toaCaseName("Bad Frog Brewery, Inc. v. New York State Liquor Authority,")
// toaCiteLine("134 F.3d 87 (2d Cir. 1998)", "14, 15")
//
// toaCaseName("Brooklyn Branch of Nat'l Ass'n for the Advancement of Colored People v. Kosinski,")
// toaCiteLine("735 F. Supp. 3d 421 (S.D.N.Y. 2024)", "20")
//
// For statutes (not italicized):
// function toaStatuteName(name) {
//   return new Paragraph({
//     spacing: { line: 240, after: 0 },
//     children: [new TextRun({ text: name, font: FONT, size: SZ })],
//   });
// }
// toaStatuteName("U.S. Const. amend. I")
// toaCiteLine("", "passim")   // or with a specific citation if needed
//
// After the last TOA entry, insert a page break:
// new Paragraph({ children: [new PageBreak()] })
```

**Caption block with case number right-aligned:**
```js
// "v." on left, case number on right, same line
new Paragraph({
  spacing: { line: 240, after: 120 },
  tabStops: [{ type: TabStopType.RIGHT, position: TabStopPosition.MAX }],
  children: [
    new TextRun({ text: "v.", font: FONT, size: SZ }),
    new TextRun({ text: "\tCivil Action No. __________", font: FONT, size: SZ }),
  ],
})
```

**Signature block (/s/ for ECF):**
```js
["/s/ [Attorney Name]", "[Attorney Name] (Bar No. ______)", "[Firm Name]", "[Address]", "[Phone] | [Email]", "Attorneys for [Party]"].forEach(line => {
  new Paragraph({
    spacing: { line: 240, after: 0 },
    alignment: AlignmentType.RIGHT,
    children: [new TextRun({ text: line, font: FONT, size: SZ })],
  });
});
```

**Horizontal rule (caption divider):**
```js
new Paragraph({
  border: { bottom: { style: BorderStyle.SINGLE, size: 6, color: "000000", space: 1 } },
  spacing: { after: 360 },
})
```

**Point headings (hanging indent, single-spaced, bold):**
```js
// Point headings use a hanging indent so wrapped lines align with the text, not the numeral.
// They are single-spaced (line: 240) and bold, with space before to separate from prior content.
//
// Level 1 (I., II., III.):  left: 720,  hanging: 720
// Level 2 (A., B., C.):    left: 1440, hanging: 720
// Level 3 (i., ii., iii.): left: 2160, hanging: 720
//
// The "left" value is the total indent from the page margin to where wrapped text aligns.
// The "hanging" value pulls the first line (the numeral) back to the left of that.
// So for Level 1: the numeral "I." starts at 0 twips (720 - 720), text starts at 720 twips.
// For Level 2: the numeral "A." starts at 720 twips (1440 - 720), text starts at 1440 twips.

function pointHeading(numeral, text, level = 1) {
  const LEFT_PER_LEVEL = 720; // 0.5 inch per level
  const HANGING = 720;
  const left = LEFT_PER_LEVEL * level;
  return new Paragraph({
    spacing: { line: 240, before: 120, after: 240 },
    keepNext: true,
    indent: { left, hanging: HANGING },
    children: [
      new TextRun({ text: `${numeral}\t${text}`, font: FONT, size: SZ, bold: true }),
    ],
    tabStops: [{ type: TabStopType.LEFT, position: left }],
  });
}
// Usage:
// pointHeading("I.", "Plaintiffs Have Partnered With Restaurants And Delivery Workers To Drive Enormous Benefits For New Yorkers.", 1)
// pointHeading("A.", "The Minimum Pay Rule Already Compensates Workers.", 2)
// pointHeading("i.", "Workers received sizeable pay increases.", 3)
//
// IMPORTANT: Use \t between the numeral and the heading text so the tab stop
// aligns the text consistently. The tabStop at position `left` ensures the
// text portion begins at the hanging-indent baseline.
```

```js
// Section titles (PRELIMINARY STATEMENT, ARGUMENT, CONCLUSION, etc.)
// CRITICAL: Always set keepNext: true so titles are never orphaned at page bottom.
function sectionTitle(text) {
  return new Paragraph({
    alignment: AlignmentType.CENTER,
    spacing: { line: 480, before: 120, after: 240 },
    keepNext: true,
    children: [
      new TextRun({ text, font: FONT, size: SZ, bold: true, allCaps: true, underline: {} }),
    ],
  });
}
```

