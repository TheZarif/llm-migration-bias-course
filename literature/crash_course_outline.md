# Crash Course Outline: LLM Bias, Stereotypes, IR, and Migration

This outline keeps the original 12 modules and expands the readings inside each module. Readings are grouped as core and supplemental so we can stay interactive without drowning in papers.

## 1. Framing the Problem: What Is Bias in LLMs?

Core:
- Bender et al. (2021), "On the Dangers of Stochastic Parrots"
- Gallegos et al. (2024), "Bias and Fairness in Large Language Models: A Survey"
- Caliskan et al. (2017), "Semantics derived automatically from language corpora contain human-like biases"
- Fiske et al. (2002), Stereotype Content Model
- Blumer (1958), group position theory

Supplemental:
- Data Statements for NLP; Datasheets for Datasets; Model Cards
- Allport (1954), "The Nature of Prejudice"; Tajfel and Turner (1979), social identity theory

Why it matters:
This module establishes bias as a measurement, documentation, harm-framing, and intergroup-relations problem, not just a bad-output problem.

## 2. How Bias Shows Up in Language Models

Core:
- Sheng et al. (2019), "The Woman Worked as a Babysitter"
- Sap et al. (2019), "The Risk of Racial Bias in Hate Speech Detection"
- Hofmann et al. (2024), "AI generates covertly racist decisions about people based on their dialect"
- Haslam (2006), "Dehumanization"
- Esses et al. (2013), media, threat, and dehumanization of immigrants and refugees

Supplemental:
- Social Bias Frames; ToxiGen; DecodingTrust; Cuddy et al. (2007), BIAS map

Why it matters:
For migration, bias may appear as explicit stereotypes, subtle toxicity, differential sentiment, dialect penalties, refusal asymmetry, or decision disadvantage.

## 3. Classic Bias Benchmarks

Core:
- StereoSet; CrowS-Pairs; BBQ; BOLD; HONEST; HolisticBias; UNQOVER

Supplemental:
- WinoBias; embedding-bias papers by Bolukbasi et al. and Gonen & Goldberg

Why it matters:
These papers give you the design vocabulary for controlled probes: minimal pairs, stereotype choices, ambiguous contexts, open-ended continuations, and descriptor inventories.

## 4. Prompting and Experimental Design

Core:
- BBQ
- UNQOVER
- Marked Personas
- Red Teaming Language Models to Reduce Harms

Supplemental:
- HELM; DecodingTrust

Why it matters:
This module turns benchmark ideas into experimental recipes: prompt templates, perturbations, adversarial probes, repeated sampling, and multi-metric evaluation.

## 5. Bias Beyond Protected Attributes

Core:
- HolisticBias
- Marked Personas
- Global Voices, Local Biases
- Hofmann et al. (2024) on dialect
- Lee and Fiske (2006), immigrants in the Stereotype Content Model

Supplemental:
- Data Statements for NLP; CIVICS; Fiske et al. (2002); Blumer (1958)

Why it matters:
Migration bias is often indirect: nationality, accent, language variety, name origin, religion, class, legal status, or education history may act as proxy cues.

## 6. Migration as a Research Domain

Readable module draft: `literature/modules/module-06-migration-as-research-domain.md`

Core:
- Zhu et al. (2024), nationality bias in ChatGPT
- CIVICS
- PapersPlease
- Digital Gatekeepers
- Hainmueller and Hopkins (2014), "Public Attitudes Toward Immigration"
- De Genova (2002), migrant illegality and deportability
- Menjivar and Abrego (2012), legal violence

Supplemental:
- Whose Opinions Do Language Models Reflect?
- Global Voices, Local Biases
- Brader et al. (2008); Sniderman et al. (2004); Esses et al. (1998); Hopkins (2010)

Why it matters:
This module maps the migration system itself: migrant categories, actors, institutions, variables, outcomes, and concrete sites where LLMs may enter information access or decision workflows.

## 7. LLMs as Decision-Makers and Decision Aids

Readable module draft: `literature/modules/module-07-llms-as-decision-aids.md`

Core:
- Tamkin et al. (2023), "Evaluating and Mitigating Discrimination in Language Model Decisions"
- PapersPlease
- Digital Gatekeepers
- The Silicon Ceiling

Supplemental:
- Hofmann et al. (2024); Wang et al. (2025) on misportraying identity groups

Why it matters:
This is where representational bias becomes allocative harm: who gets admitted, helped, believed, ranked, flagged, or denied.

## 8. IR Angle: Retrieval, Ranking, and Summarization Bias

Core:
- FA*IR
- Fairness of Exposure in Rankings
- Fairness in Ranking: A Survey
- Auditing Search Engines for Differential Satisfaction Across Demographics
- Entman (1993), framing
- Eberl et al. (2018), European media discourse on immigration

Supplemental:
- Perspectival Mirror of the Elephant
- Learning the Topic, Not the Language
- Scheufele (1999); Boomgaarden and Vliegenthart (2009)

Why it matters:
For IR, the key question is not only what the model says, but what it retrieves, ranks, summarizes, cites, omits, or overexposes.

## 9. Multilingual and Cross-Cultural Issues

Core:
- CIVICS
- Global Voices, Local Biases
- Learning the Topic, Not the Language
- Perspectival Mirror of the Elephant
- Eberl et al. (2018)

Supplemental:
- HONEST; Data Statements for NLP; Hainmueller and Hopkins (2014)

Why it matters:
Migration discourse is locally framed. English-only prompts can erase local politics, legal categories, and community-specific terms.

## 10. Methods You Could Use in Your Own Research

Core method families:
- Pairwise stereotype probes: CrowS-Pairs, WinoBias, Bolukbasi et al.
- Ambiguous QA: BBQ, UNQOVER
- Open-ended generation: BOLD, HONEST, Sheng et al.
- Decision audits: Tamkin et al., PapersPlease, Digital Gatekeepers
- Ranking audits: FA*IR, Fairness of Exposure, search-engine auditing
- Cultural/multilingual audits: CIVICS, Global Voices, Learning the Topic
- Social-science-driven audits: Stereotype Content Model, threat cues, dehumanization, framing, legal violence

Why it matters:
This module converts readings into experiment templates you can adapt.

## 11. Open Problems and Research Opportunities

Core:
- Bias and Fairness in LLMs survey
- Stochastic Parrots
- Wang et al. (2025), LLMs replacing human participants
- Whose Opinions Do Language Models Reflect?

Research gaps:
- Migration-specific LLM benchmarks remain thin.
- IR-style exposure and source-diversity metrics are underused in LLM migration-bias work.
- Legal status, asylum status, and nationality are often conflated.
- Multilingual evaluation still tends to lag behind English-centric work.
- Social-science constructs such as threat, group position, dehumanization, and legal violence are rarely operationalized in LLM benchmarks.

## 12. Your Research Direction Workshop

Possible project directions:
- Build a BBQ-style immigration adjudication benchmark.
- Audit LLM-assisted retrieval for migration-related queries across languages.
- Compare humanitarian, security, economic, and criminality frames in generated summaries.
- Test whether nationality, dialect, name origin, or visa status changes LLM decisions.
- Evaluate LLM-as-annotator reliability for migration discourse classification.

Suggested deliverables:
- A scoped research question.
- A dataset design.
- A metric suite.
- A risk and ethics note.
- A short related-work map anchored in the expanded bibliography.
