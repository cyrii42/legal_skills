---
name: deposition-summary
description: Produce a structured, litigation-ready summary of a deposition transcript for plaintiffs-side litigation. Use when the user wants to summarize, digest, or condense deposition testimony that has already been given. Triggers on phrases like "summarize this deposition," "depo summary," "digest this transcript," or "summarize [name]'s testimony."
---

# Deposition Summary

Produces a structured, litigation-ready summary of a fact, 30(b)(6), or expert deposition transcript, as internal attorney work product for plaintiffs-side litigation. The summary is practice-area-neutral: it works for any plaintiffs-side matter (antitrust, securities, consumer, employment, data breach, environmental, whistleblower, and so on).

The default deliverable is a Word (.docx) document. The user can ask for a different format.

Work through the steps below in order. Do not skip the context and purpose steps: what the summary should emphasize depends on them.

## Core principles (read first)

These govern everything below and are non-negotiable:

- **Never invent testimony.** Every factual assertion, characterization, and quotation must trace to the transcript (or, for exhibit identification, to an uploaded exhibit or the record). If you cannot point to the source, do not write it. When you are uncertain, say so: a flagged gap is correct; a confident fabrication is a serious failure.
- **Do not characterize beyond the record.** Report what the witness said. Call an admission an admission and an inconsistency an inconsistency, but do not embellish, minimize, or infer facts that the testimony does not support.
- **Cites must be real.** See "Citation discipline" below. A clean-looking but wrong page:line cite is worse than no cite, because a reader may rely on it in a brief.

## Step 1: Establish case context

The analytical parts of the summary (overview/assessment, favorable admissions, harmful testimony, follow-up) require knowing the case theory. The factual parts do not. So first determine what context you have. There are three entry states; handle whichever applies:

1. **Context already present.** You are working inside a project, workspace, or conversation that already contains the operative complaint or other case materials (or the user has described the case). Use it.
2. **Case documents supplied with the request.** The user uploaded or attached case materials (a complaint, scheduling order, prior ruling, case memo) alongside the transcript. Use them.
3. **No context.** You have only a transcript.

**If you are in state 3, do not interrogate the user with a questionnaire.** Instead, walk this ladder, stopping as soon as you have enough:

- Ask for the **operative complaint** first, and/or any other document that would orient the summary (scheduling order, a key prior ruling, a short case memo). This is the best context.
- If the user cannot or will not supply documents, accept **one or two sentences of free-text context** (what the case is about and what they need from this witness) and proceed on that.
- If the user gives nothing at all, proceed in **facts-only fallback mode** (see Step 2). Do not block the user.

**What counts as "sufficient context" to unlock the analytical layer:** you have enough context when you can articulate, in your own words, the operative claims or theories in the case and what is at stake for this particular witness. If you cannot, you are in facts-only mode, regardless of entry state.

## Step 2: Determine the output purpose

The skill produces one of three outputs. Pick the default unless the user names a purpose; the user can switch at any time.

- **Facts-only summary:** the factual layer alone (witness background, testimony by topic, exhibits, notable quotes, and context-free credibility signals). It has **no** overview/assessment, favorable, or harmful sections. This is also the mandatory shape of the no-context fallback, but the user may choose it deliberately even when context exists (for example, for a neutral reference, or something to hand to someone who should not receive work-product characterizations).
- **Quick read:** condensed. A short overview/assessment, the headline testimony by topic in compressed form, the top handful of admissions and harmful points, and the most important quotes. The gist, fast. (Requires context for the analytical parts.)
- **Full work-product summary:** the comprehensive artifact. All topics developed, full cite support, all analytical sections, follow-up. (Requires context.)

**Default:** Full work-product summary when you have sufficient context (Step 1); Facts-only when you do not.

## Step 3: Ingest the transcript(s)

**Multiple volumes or sessions.** One summary covers one deponent. If the deposition spans multiple volumes or days, accept all of that deponent's transcript files and integrate them into a single summary; disambiguate citations by volume or date (see Citation discipline). Different witnesses get separate summaries (separate runs).

**Detect and announce the transcript type.** Before drafting, identify what you were given and say so at the top of your working process and in the metadata block:

- **Full-page certified transcript** (one page per page, line-number gutter): most reliable.
- **Condensed / "min-U-script" (4-up):** four mini-pages tiled per sheet. Page:line mapping is easy to misread here, so be careful and flag it.
- **Rough / realtime ASCII (uncertified):** pagination may be provisional; verify quotes before relying on them.
- **Scanned / OCR'd:** text may contain OCR errors, and page:line may be unreliable.

**Nudge once on low-reliability formats.** If the transcript is condensed, scanned, or rough, tell the user once that the court reporter can almost always provide a clean full-page PDF and an e-transcript (.txt/.ptx), and that citations will be far more reliable from those. Then proceed on whatever you have; do not block the user.

**Detect the witness type** (usually stated on the record) and adjust emphasis modestly. The core structure stays the same; these are light overlays:

- **Fact witness:** the default; no overlay.
- **30(b)(6) designee:** testimony given in the corporate-representative capacity binds the *organization*. It is a party admission of the entity, often more valuable than a personal statement. Where an admission was given in that capacity, note that it binds the entity. (This is a context-gated characterization; include it only in analytical mode.)
- **Expert:** add treatment of the witness's opinions, their stated bases and methodology, and any concessions on cross.

**Very long transcripts.** Read the transcript in full when it fits. When it is too long to take in reliably in one pass, read it in **ordered sections** and build the summary incrementally, and say plainly in the output that you processed it in N parts. **Never silently truncate.** After section-wise reading, run a **cross-section reconciliation pass**: compare across the whole transcript for internal contradictions (a witness who says X early and not-X late), because the credibility layer requires whole-transcript awareness that section-by-section reading would otherwise lose. If even section-wise processing strains, tell the user and ask them to designate the portions to prioritize, but make that the announced exception, not the default.

## Step 4: Read, analyze, and (if provided) review exhibits

As you read, organize testimony into subject-matter buckets (this is a factual operation and needs no case context) and capture:

- **Witness background:** role, tenure, responsibilities relevant to the matter.
- **Testimony by topic:** what the witness said, bucketed by subject.
- **Exhibits:** every marked exhibit, its identification, and the testimony about it.
- **Notable verbatim quotes:** self-contained exchanges worth preserving (see Quote rules).
- **Internal credibility signals:** within-transcript contradictions, implausible "I don't recall" patterns, evasiveness. *These are context-free and appear even in facts-only mode.*
- If you have context: **favorable admissions**, **harmful testimony**, and material for the **overview/assessment** and **follow-up**.

**Exhibit review triage (when exhibit files are uploaded).** Look at the exhibits, but do not ingest them wholesale:

- **Read the relevant portions of exhibits that the testimony turns on** (an exhibit tied to a key admission, harmful testimony, or a genuinely contested topic). The transcript points you to what was discussed (a specific paragraph, figure, or email in a chain); read that. Read enough to (i) identify the document accurately and (ii) check the witness's characterization of it against what the document actually says.
- **Identification-only for peripheral exhibits:** capture type/date/author/Bates from the face plus the on-record description; do not read through them.
- **Never read a large exhibit end to end** just because it was uploaded. A 200-page exhibit that the witness touched once gets its one relevant section read, not all 200 pages.
- **Flag partial review** where a reader might otherwise assume that you read an exhibit in full.
- Where the witness's characterization of a document diverges from the document itself, note it (context-gated, because "divergence matters" leans on the case theory).

Do not fabricate exhibit descriptions. If neither the record nor an uploaded copy identifies an exhibit, say that the record does not identify it rather than guessing.

## Step 5: Draft the summary

Produce the summary in clean Markdown first (this is also the fallback deliverable if Word generation fails). Use this section set and **order**. Depth scales with the chosen purpose (Step 2).

Sections marked **(context-gated)** appear only in analytical mode (Quick read or Full). In facts-only/fallback mode, omit them entirely. Sections marked **(factual)** always appear.

1. **Metadata block** *(factual)*: a header block giving case name and docket (if known), deponent name and role/title, deposition date, date prepared, summary type (facts-only / quick read / full), and a transcript-type/reliability note. Above it, the document carries the confidentiality legend (handled by the docx builder; in Markdown, put it as the first line).
2. **Overview & Assessment** *(context-gated)*: **at the very top of the body.** A narrative section (not a bullet box) giving a brief overview of the deposition and the attorney-facing strategic assessment together: what this deposition established or failed to establish, and the significant takeaways for the litigation. Direct and analytical. In Quick read, a tight few sentences; in Full, developed.
3. **Witness background** *(factual)*: role, tenure, responsibilities. Cite key page:line.
4. **Testimony by topic** *(factual)*: the spine. One subheading per subject-matter bucket, narrative summary in past tense with inline page:line cites. Cross-reference exhibits by number where the witness's testimony about a document matters to the topic (identification lives in the Exhibits table, not repeated here).
5. **Exhibits** *(factual)*: a reference table, one row per marked exhibit, plus the inline cross-references in section 4. See the table format below.
6. **Notable verbatim quotes** *(factual capture)*: self-contained Q&A excerpts. See Quote rules. In facts-only mode, select the passages of clearest, most substantive testimony (rather than "brief-worthy"); the inclusiveness rules are identical.
7. **Internal credibility signals** *(factual, context-free)*: bulleted. Within-transcript contradictions (cite both conflicting passages), implausible non-recall, evasiveness. If none, say so in one sentence rather than omitting the section.
8. **Favorable admissions** *(context-gated)*: bulleted. Each a concise statement of what the witness admitted, with a cite; verbatim only where the exact words matter. For a 30(b)(6) designee, note where an admission binds the entity.
9. **Harmful testimony** *(context-gated)*: bulleted. Framed objectively ("[Witness] testified that..."), accurate, not minimized. The attorney assesses weight.
10. **Follow-up items** *(context-gated)*: **at the end.** Bulleted: documents referenced but not produced, witnesses identified who should be pursued, factual claims needing corroboration, contradictions with produced documents worth pressing. If none are apparent, say so in one sentence.

**Exhibits table format:**

| Exhibit | Identification | First used | Testimony |
|---------|----------------|-----------|-----------|
| Ex. 1 | [Type, date, author/recipient, Bates range, only where stated on the record or visible on the face] | [page:line] | [One- to two-sentence summary of the testimony about it] |

### Quote rules

Quotes must be inclusive enough to stand on their own, and never a stripped soundbite:

- Capture the **framing question(s)**, the answer, and any **immediately following qualification, hedge, walk-back, or clarification** that the witness added. If reading only the excerpt would mislead someone about what the witness actually said, include more context, not less.
- If an admission is **built across several Q&A pairs**, include the whole run, even at the cost of length.
- **Hard integrity rule:** never clip in a way that omits a qualification that changes the meaning. If the witness hedged it or took it back two lines later, the excerpt must show that.
- The citation spans the **full excerpt**. Where you trim genuinely irrelevant intervening colloquy, mark it with an ellipsis (...); never silently splice.
- Bias toward over-inclusion: a slightly-too-long quote costs a few lines; a misleadingly short one can put a bad citation in a brief.

Format each quote as a block quote with the citation on its own line beneath, with no leading dash:

> Q: [exact question text]
>
> A: [exact answer text]
>
> [Deponent surname] Dep. [page]:[line]–[page]:[line]

### Citation discipline

- **Quote-anchored cites, always and in every mode.** Cite a page:line only if you can point to the verbatim anchor text there. If you cannot locate the language, do not emit a cite.
- **Format:** single line `(Dep. 45:12.)`; line range `(Dep. 45:12–14.)`; page range `(Dep. 45:12–46:3.)`. Where the deponent's name is needed for clarity, `(Smith Dep. 45:12–14.)`. For multi-volume, disambiguate: `(Dep. Vol. II, 45:12.)` or by date `(3/15 Dep. 45:12.)`.
- **When a page:line cannot be confidently pinned** (condensed, scanned, or rough transcript), flag it rather than emitting a clean-looking cite. For example: `(Dep. 87 [page uncertain]; verify against certified transcript.)`. Never fake precision, and never approximate a cite with a stray symbol.

## Step 6: Verify before delivering

- **Quote-anchor check (every output):** confirm that each cite corresponds to real anchor text in the transcript. Drop or flag any that you cannot confirm.
- **Verification pass (full work-product summary):** re-locate every citation in the source and confirm that the quoted or paraphrased language is actually there. This is a distinct pass over the drafted summary, not a re-read of the transcript in the abstract.
- Confirm that no section characterizes beyond the record, and that every context-gated section is actually supported by the case context you have.
- The output carries a standing caveat to verify all citations against the certified transcript before filing.

## Step 7: Deliver

**Default: a Word (.docx) document.** Once the Markdown summary is complete and verified, convert it with the bundled builder:

- The builder is `scripts/build_docx.py` in this skill's directory. It needs `python-docx`.
- Where a shell with `uv` is available (for example, a local Claude Code session): `uv run --script <skill-dir>/scripts/build_docx.py <summary.md> [output.docx]` (the script header provisions `python-docx`).
- Otherwise (for example, a hosted code or analysis environment): ensure that `python-docx` is installed, then run or import `build_docx.py` and call `build(md_path, out_path)`.
- The builder applies the house style: Times New Roman 12pt; bold, section-numbered headings at body size; 1-inch margins; footer page numbers; left-aligned, single-spaced body; and the "Privileged & Confidential - Attorney Work Product" legend at the top.

**If Word generation fails for any reason, hand the user the clean Markdown summary** rather than erroring out. Do not leave a non-technical user with nothing.

**Overrides:** if the user asks for a different format (Markdown, plain text, a rendered document, and so on), give them that instead of the .docx.

## Writing standards

**Integrity guardrails** (see Core principles) are paramount and non-negotiable.

**Style** (a neutral, defensible-anywhere subset; do not impose more than this):

- Objective tone in the factual sections; direct and analytical in the context-gated sections.
- Past tense throughout ("The witness testified that...," "Smith stated that...").
- Active voice; name who acted.
- Oxford comma; en-dashes for numeric ranges (45:12–14).
- Keep the complementizer "that" ("testified that...," "conceded that...").
- Refer to judges by honorific plus surname if they come up ("Judge Smith").
- Avoid AI-writing tells (delve, navigate, leverage, robust, comprehensive, seamless, tapestry, myriad, "not just X but Y," and the em-dash used in place of a colon).
- This is internal work product; do not over-polish. Legibility over flourish.

## Reference

`reference/example-full-summary.md` is a gold-standard full summary over synthetic, invented facts (a fictional company and witness). Consult it for format, depth, tone, and citation style. Do **not** treat its facts, topics, or wording as a template to fill in: it illustrates the shape, not a form.
