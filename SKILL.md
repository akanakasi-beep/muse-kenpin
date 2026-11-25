# 検品 (Kenpin) — Claim–Record Verification

Verify claims against records and original sources, and return the result with its grounds. The deliverable is not an opinion; it is a collation result: what matches, what does not, and what has no source at all.

## When to use

- The user asks you to check, verify or fact-check a claim, article, report, proposal, résumé, AI output or tip.
- A document makes factual claims (numbers, dates, quotations, attributions) that a decision will rest on.
- Someone asserts something strongly ("this will definitely go up", "the data shows…") without showing grounds.

Use ordinary web search for general questions. Use this skill when the point is the *collation itself* — claim by claim, against the record.

## The protocol

1. **検知 (Detect)** — State what is being claimed, in one line. Separate the claim from the person claiming it.
2. **検品 (Extract)** — Break the claim into checkable units: numbers, dates, names, quotations, causal assertions. Untestable parts are labelled untestable, not silently dropped.
3. **照合 (Collate)** — Match each unit against the original source or record.
   - A reference existing is not the same as the original being checked. "A source was cited" and "the cited original actually says this" are two different results; report which one you reached.
   - Trace quotations and figures to the primary source when one exists. A summary of a summary is a lead, not evidence.
   - Distinguish three kinds of agreement: same page pointing at the same thing / two sources independently pointing at the same thing / one source repeated many times.
4. **復元 (Restore)** — Reconstruct what the source actually says, in context, where the claim distorted it (dropped conditions, shifted scope, changed a "may" into a "will").
5. **補完 (Complete)** — Fill gaps only with labelled inference. Inference is marked as inference, with its branching point named.
6. **記録 (Record)** — Write the result in the four-point format below. Never edit the record afterwards to look better; corrections are appended as new lines, and a wrong verdict stays visible with its correction.

## Output format (four points)

1. **結論 (Conclusion)** — Per claim: 一致 (matches) / 不一致 (does not match) / 出典なし (no source) / 検品不能 (cannot be verified, with the reason). No overall grade that hides the per-claim results.
2. **根拠 (Grounds)** — The sources actually checked, with enough reference (title, date, URL or record location) for the user to re-check them. Only sources you opened count.
3. **推論の分岐点 (Where inference branches)** — The points where the result depends on interpretation rather than the record, and what would change the verdict.
4. **未解決 (Unresolved)** — What could not be checked and why (no access, source does not exist, claim too vague), stated plainly.

## Rules

- **No source, no verdict.** If a claim has no checkable source, say 検品不能. Never fill the gap with a plausible-sounding answer.
- **Attribution is checked, not assumed.** Who first proposed an idea and who proposed the decisive move are separate facts. Credit follows the record of who said what first, not who wrote the final text.
- **Collation, not evaluation.** Presenting whether a claim matches its source is the product. Judgements that belong to regulated advice (e.g. "this stock is cheap", "buy now") are outside the verdict; in finance, stay on the collation of disclosed facts against claims.
- **Numbers are re-read, not remembered.** Any figure the user may act on is checked against the source in this session, with its date and conditions.
- **Absence is a result.** Finding nothing is reported as finding nothing — never upgraded into "probably fine" and never downgraded into "probably false".
- **Quote minimally.** Short fragments only, attributed to their source. Summarise the rest.

## Working style

- Check the decisive claims first: the ones the user's decision actually turns on.
- Report in the user's language, briefly. The four-point format is the depth; the prose around it stays short.
- Save the full record to a file when the result may be revisited, and name the file by topic and date.
