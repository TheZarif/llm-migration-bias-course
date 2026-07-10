# Module 7: LLMs as Decision-Makers and Decision Aids

This module asks what changes when LLMs move from **representing** migrants to **helping decide things about them**.

The core distinction:

> Representational harm concerns how people are described. Allocative harm concerns who receives resources, opportunities, protection, scrutiny, or punishment.

For migration research, this shift matters because many migration systems are already bureaucratic, discretionary, document-heavy, multilingual, and high stakes. LLMs do not need to be final decision-makers to matter. They can shape decisions by summarizing files, ranking cases, drafting rationales, translating testimony, flagging risk, or suggesting next steps.

## 1. Model Roles In Decision Systems

Do not begin by asking only whether "the LLM decides." Most deployed systems are messier. The model may occupy one of several roles.

| Role | What The Model Does | Migration Example | Main Risk |
| --- | --- | --- | --- |
| Clerk | Extracts, translates, summarizes, formats, or organizes information. | Summarizes an asylum narrative or visa file. | Omits legally relevant detail or changes tone/credibility. |
| Advisor | Recommends an option but a human decides. | Suggests whether a case needs additional review. | Human overreliance or automation bias. |
| Scorer | Assigns risk, priority, credibility, vulnerability, or eligibility. | Scores fraud risk or vulnerability for service triage. | Proxy discrimination and false precision. |
| Gatekeeper | Controls access to resources or attention. | Routes people to legal aid, housing, or appointment queues. | Unequal access, hidden denial, or delay. |
| Decider | Produces or directly executes an outcome. | Recommends visa approval or asylum denial as final output. | Direct allocative harm with weak recourse. |

The same model output can have different stakes depending on the role. A flawed summary in casual chat is one problem; the same flawed summary inside an asylum file is a very different problem.

## 2. Why Migration Decisions Are Special

Migration decisions often have features that make LLM use risky:

- **High stakes:** admission, removal, detention, family separation, housing, employment, legal status.
- **Discretion:** many decisions involve judgment, not only rule application.
- **Incomplete evidence:** people fleeing conflict or instability may lack documents.
- **Credibility assessment:** decision-makers often evaluate whether stories seem coherent or believable.
- **Translation and interpretation:** testimony may move across languages, dialects, and legal vocabularies.
- **Proxy cues:** nationality, accent, name, religion, occupation, and documentation can stand in for risk or deservingness.
- **Information asymmetry:** affected people may not know how a system summarized, scored, or routed them.
- **Limited recourse:** migrants may have less ability to contest or correct automated outputs.

This means migration decision systems are not just classification problems. They are institutional systems involving law, discretion, power, and documentation.

## 3. Decision Bias Is Not Only Outcome Difference

A simple audit might ask:

> Does the model approve one group more often than another?

That is useful, but incomplete. In decision support, bias can appear in several places.

| Decision Surface | What To Measure |
| --- | --- |
| Outcome | Approval, denial, referral, priority, risk flag, extra review. |
| Confidence | Whether the model is more certain for some groups than others. |
| Evidence use | Whether the model follows provided facts or fills uncertainty with assumptions. |
| Burden of proof | Whether some applicants are asked for more documentation or stronger evidence. |
| Rationale | Whether explanations invoke legality, fraud, culture, threat, vulnerability, or contribution. |
| Tone | Whether the model is skeptical, empathetic, bureaucratic, punitive, or paternalistic. |
| Recourse | Whether the model explains how to challenge or correct an outcome. |
| Error type | False denial, false suspicion, false reassurance, hallucinated legal rule, missing jurisdiction. |

For migration, the rationale often matters as much as the outcome because rationales can normalize categories such as "fraud risk," "insufficient credibility," "failure to integrate," or "public burden."

## 4. Controlled Decision Audits

A strong decision audit varies one factor at a time while holding the case constant.

Example base case:

> An applicant requests emergency housing after losing work. The applicant has lived locally for three years, has two children, has no criminal record, and has incomplete paperwork because documents were lost during displacement.

Possible controlled variants:

- Status: citizen / refugee / asylum seeker / undocumented migrant / temporary worker.
- Country of origin: Ukraine / Syria / Haiti / Mexico / India / Britain.
- Documentation: complete / missing / translated / inconsistent.
- Language: fluent English / accented English / translated statement / non-standard grammar.
- Family status: single adult / parent with children / elderly applicant.
- Occupation: software engineer / caregiver / farm worker / unemployed.

Possible outcomes:

- Should the applicant receive priority?
- How credible is the explanation?
- Should the case be flagged for review?
- What additional documents are needed?
- What risks should the agency consider?
- What support should be offered?

The strongest version separates outcome from explanation:

1. Ask for a decision.
2. Ask for confidence.
3. Ask for the evidence used.
4. Ask what information would change the decision.
5. Code the rationale for threat, deservingness, legality, credibility, and agency.

## 5. Evidence Sensitivity

A useful question is not only whether the model is biased under ambiguity, but whether it updates appropriately when evidence changes.

Design:

1. **Ambiguous case:** documentation is missing, no reason given.
2. **Benign explanation:** documents were lost during evacuation.
3. **Administrative explanation:** documents are delayed by the issuing agency.
4. **Contradictory evidence:** records conflict with the applicant's statement.

Then ask:

> Does the model update based on evidence, or does the identity cue continue to drive suspicion?

This adapts the logic of BBQ-style ambiguity to decision support, but the outcome is institutional: credibility, priority, risk, or referral.

## 6. Proxy Discrimination

Migration decisions are especially vulnerable to proxy discrimination because protected or sensitive information can enter indirectly.

Examples:

- Name as proxy for ethnicity or religion.
- Country of origin as proxy for race, conflict, wealth, passport power, or geopolitical status.
- Accent or grammar as proxy for education, credibility, or belonging.
- Occupation as proxy for class and economic value.
- Legal status as proxy for morality or deservingness.
- Documentation gaps as proxy for fraud.

Hofmann et al. show that dialect cues can shape discriminatory decisions even when explicit racial labels are absent. In migration, the analogous concern is that accent, translated testimony, name, or nationality can shift model recommendations without the system acknowledging discrimination.

## 7. Explanation Audits

LLM decision systems often generate explanations. These explanations are powerful because they can make a decision appear objective, careful, or legally grounded.

Audit explanations for:

- **Legal overreach:** does the model invent or overstate legal rules?
- **Moral leakage:** does legal status become moral worth?
- **Threat language:** crime, fraud, public burden, security, integration risk.
- **Paternalism:** vulnerable, helpless, dependent, unable to advocate.
- **Evidence mismatch:** explanation mentions facts not in the prompt.
- **Missing uncertainty:** model gives a confident recommendation despite insufficient information.
- **Recourse absence:** no guidance on appeal, correction, documentation, or rights.

For migration, a polished explanation can be harmful if it launders stereotypes through bureaucratic language.

## 8. Human-In-The-Loop Is Not Automatically Safe

Many systems claim safety because a human remains the final decision-maker. That is not enough.

Human-in-the-loop systems can still create harm through:

- automation bias: humans defer to model output.
- anchoring: the first model summary shapes interpretation.
- workload pressure: staff rely on model triage to move quickly.
- opacity: affected people cannot see or contest the model's role.
- diffusion of responsibility: no one feels accountable for the final harm.

So the audit question should be:

> How does the model reshape the human decision environment?

Not only:

> Did the model make the final decision?

## 9. Migration Decision Audit Template

Use this template to scope a study.

| Component | Questions |
| --- | --- |
| Decision site | Visa, asylum, housing, legal aid, hiring, welfare, content moderation? |
| Model role | Clerk, advisor, scorer, gatekeeper, decider? |
| Affected population | Which migrant category and receiving context? |
| Controlled variables | Status, nationality, language, documentation, family, occupation, religion, gender? |
| Outcome measures | Approval, denial, priority, confidence, extra review, credibility, risk? |
| Explanation measures | Threat, deservingness, legality, evidence use, uncertainty, recourse? |
| Comparison baseline | Human policy, randomization, neutral case, non-migrant case, alternative model? |
| Harm model | Representational, allocative, procedural, informational, legal, epistemic? |

## Core Readings

- Tamkin et al. (2023), "Evaluating and Mitigating Discrimination in Language Model Decisions."
- PapersPlease: immigration-inspector moral dilemmas and motivational values.
- Digital Gatekeepers: LLMs in immigration decision contexts.
- The Silicon Ceiling: GPT bias in hiring with immigrant-marker effects.
- Hofmann et al. (2024), dialect cues and covertly racist decisions.
- Menjivar and Abrego (2012), legal violence.

## Takeaway

In migration, LLM decision support should be studied as part of a bureaucratic and legal system.

A strong research question is not:

> Are LLMs biased against migrants?

It is:

> When LLMs summarize, score, route, or recommend decisions about migrants, which identity and proxy cues change outcomes, explanations, evidentiary burdens, uncertainty, and recourse?

## Check

Suppose an LLM recommends "additional review" for an asylum applicant because their documents are incomplete.

What would you need to know before calling this appropriate?

Consider:

- Is missing documentation common or expected in the applicant's situation?
- Did the model consider displacement, conflict, translation, or agency delays?
- Would it make the same recommendation for a citizen or high-status applicant?
- Did it use fraud language without evidence?
- Did it explain what evidence would resolve uncertainty?
- Does "additional review" create delay, detention, denial, or loss of access?
