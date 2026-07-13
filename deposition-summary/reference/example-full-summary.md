<!-- GOLD-STANDARD EXAMPLE. All parties, witnesses, facts, exhibits, and page/line
citations below are invented for illustration. This shows the shape, depth, tone, and
citation style of a full work-product summary. Do not reuse its facts, topics, or wording
as a template to fill in. -->

Privileged & Confidential - Attorney Work Product

# Deposition Summary: Karen Ellison

- **Case:** Rivera v. Nimbus Data Solutions, Inc., No. 24-cv-01234 (N.D. Cal.)
- **Deponent:** Karen Ellison, Director of Information Security, Nimbus Data Solutions, Inc.
- **Capacity:** Rule 30(b)(6) corporate designee (Topics 1–4, 7) and individual fact witness
- **Deposition date:** March 18, 2025
- **Date prepared:** March 24, 2025
- **Summary type:** Full work-product summary
- **Transcript:** Full-page certified transcript (one volume). Reliable pagination.

## I. Overview & Assessment

Ellison was Nimbus's designee on its data-security policies, the 2023 penetration test, its patch-management practices, and the breach response. The deposition established the fact on which our reasonable-procedures theory turns: Nimbus received a written penetration-test report in March 2023 that flagged the unpatched vulnerability in the customer database, and it did not remediate that vulnerability until after the July 2024 breach (Dep. 88:3–90:11). Because Ellison gave that testimony as Nimbus's corporate designee, it binds the company.

Two points cut the other way and will need to be met. Ellison testified that the breach was caused by a vendor's compromised credentials rather than the unpatched vulnerability (Dep. 142:6–144:2), and she testified that Nimbus had a written incident-response plan that it followed (Dep. 171:9–172:20). The causation testimony is contestable on this record: she conceded she had not reviewed the forensic report's root-cause section (Dep. 149:14–22), so the causal attribution is not grounded in the investigation she was designated to speak to. Her credibility is also independently impaired: she disclaimed knowledge of the penetration-test findings early in the deposition and then acknowledged having reviewed the report, on the same day it issued, later in it.

On balance, the deposition advanced the reasonable-procedures claim and left the defense's causation narrative exposed. The most important follow-up is the forensic root-cause material and the vendor contract, neither of which has been produced.

## II. Witness Background

Ellison has served as Nimbus's Director of Information Security since January 2021 and has been with the company for nine years, having previously managed its network-operations team (Dep. 12:4–14:9). She reports to the Chief Technology Officer and supervises a team of six, including the personnel responsible for patch management and vendor access (Dep. 15:2–16:18). She testified that she is "the person at Nimbus most familiar with how we secure customer data" (Dep. 17:3–5).

## III. Key Factual Testimony

### Security Policy Framework

Ellison described a written information-security policy adopted in 2020 and revised annually, covering access controls, patching, and vendor management (Dep. 33:7–35:19; Ex. 3). She testified that the policy required "critical" vulnerabilities to be remediated within 30 days of identification (Dep. 41:2–12).

### The 2023 Penetration Test

Nimbus retained an outside firm to conduct a penetration test in the first quarter of 2023 (Dep. 79:11–20). The resulting report (Ex. 1) identified an unpatched vulnerability in the customer database and rated it "critical" (Dep. 84:6–15). Ellison testified that the report was delivered to her team in March 2023 (Dep. 85:22–86:4).

### Patch-Management Practices

Ellison testified that patching was tracked in a ticketing system and that "most" critical patches were applied within the policy's 30-day window (Dep. 108:3–14). She acknowledged that the database vulnerability from the 2023 report was not patched within that window, and was not patched until August 2024 (Dep. 88:3–90:11). She attributed the delay to "competing priorities" and a planned database migration that was later deferred (Dep. 91:7–93:2).

### Breach Timeline and Response

Ellison placed the intrusion in July 2024 and testified that Nimbus detected it on July 22, 2024 (Dep. 130:5–17). She testified that Nimbus followed its incident-response plan (Ex. 3) and notified affected customers within the statutory window (Dep. 171:9–174:8). She attributed the intrusion to a vendor's compromised credentials (Dep. 142:6–144:2).

## IV. Exhibits

| Exhibit | Identification | First used | Testimony |
|---------|----------------|-----------|-----------|
| Ex. 1 | Third-party penetration-test report, dated March 6, 2023 (NIMBUS_0004121–0004168, per the record) | Dep. 82:9 | Report identified the customer-database vulnerability and rated it "critical"; delivered to Ellison's team in March 2023. |
| Ex. 2 | Internal email chain, March 2023, re: pen-test findings (Bates not stated on the record) | Dep. 96:4 | Ellison acknowledged receiving the chain but testified she did not recall the specific thread; other recipients are listed on its face. |
| Ex. 3 | Nimbus Incident-Response Plan, 2024 revision (NIMBUS_0011002–0011039) | Dep. 168:11 | Ellison testified Nimbus followed the plan during the breach response. |

## V. Notable Verbatim Quotes

The admission on the unpatched vulnerability, given in Ellison's corporate capacity, with the qualification she added:

> Q: So the vulnerability the March 2023 report identified in the customer database was not patched until August of 2024. Correct?
>
> A: That's correct, it was patched in August 2024.
>
> Q: And that's more than a year after the report identified it as critical?
>
> A: Yes. I'd add that we had a migration planned that would have retired that database, so the thinking was we'd address it that way.
>
> Q: But the migration didn't happen before the breach?
>
> A: No, it was deferred.
>
> Ellison Dep. 88:3–90:11.

On the basis for the vendor-credentials causation testimony:

> Q: You testified the breach was caused by the vendor's compromised credentials. Have you read the root-cause section of the forensic report?
>
> A: I've seen the report. I don't know that I read that section closely.
>
> Ellison Dep. 149:14–22.

## VI. Internal Credibility Signals

- Ellison testified early in the deposition that she was "not aware of what the 2023 pen test found" (Dep. 62:18–20), but later acknowledged that she reviewed the report on the day it issued (Dep. 86:6–13).
- She testified that "most" critical patches were applied within the 30-day policy window (Dep. 108:3–14) but could not identify any specific critical patch other than the database vulnerability when asked (Dep. 110:2–112:9).

## VII. Favorable Admissions

- As Nimbus's corporate designee, Ellison admitted that Nimbus received a written penetration-test report in March 2023 rating the customer-database vulnerability "critical," and that the vulnerability was not remediated until August 2024, after the breach (Dep. 88:3–90:11; Ex. 1). This admission binds Nimbus.
- She admitted that Nimbus's own policy required critical vulnerabilities to be remediated within 30 days (Dep. 41:2–12), and that the database vulnerability was not (Dep. 88:3–90:11).
- She conceded that the customer database at issue was not encrypted at rest (Dep. 121:4–10).
- She conceded that she had not closely reviewed the forensic report's root-cause section on which the defense's causation position depends (Dep. 149:14–22).

## VIII. Harmful Testimony

- Ellison testified that the breach was caused by a vendor's compromised credentials rather than the unpatched database vulnerability (Dep. 142:6–144:2).
- She testified that Nimbus maintained a written incident-response plan (Ex. 3) and followed it during the breach response, including notifying affected customers within the statutory window (Dep. 171:9–174:8).
- She testified that the delay in patching resulted from a planned database migration intended to retire the vulnerable system (Dep. 91:7–93:2).

## IX. Follow-Up Items

- **Forensic root-cause material:** the forensic report's root-cause section, and any underlying investigation files, were referenced but not produced. This bears directly on the contested causation question. Address in supplemental discovery.
- **Vendor contract and access logs:** the vendor whose credentials Ellison blamed was not identified by contract on the record, and the vendor-access logs were not produced. Pursue both.
- **March 2023 email recipients (Ex. 2):** the chain lists recipients other than Ellison on its face; identify them as potential custodians and deponents.
- **Patch logs:** the ticketing-system records that would corroborate or undercut Ellison's "most patches within 30 days" testimony were not produced. Request them.

*Verify all citations against the certified transcript before relying on them in any filing.*
