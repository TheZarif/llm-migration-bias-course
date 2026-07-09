# Social Science Foundations for Migration Bias

This note adds the social-science layer that was missing from the NLP-heavy bibliography. These readings help define what to look for when an LLM talks about, ranks, classifies, or makes decisions about migrants.

## Core Concepts To Carry Into LLM Work

### Stereotype Content

The Stereotype Content Model organizes stereotypes around perceived warmth and competence. For migration, this is more useful than simply asking whether model output is positive or negative. A group may be described sympathetically but still paternalistically, for example as warm but helpless, vulnerable, or incompetent.

Key readings:
- Fiske et al. (2002), Stereotype Content Model.
- Lee and Fiske (2006), immigrants in the Stereotype Content Model.
- Cuddy et al. (2007), BIAS map linking stereotypes to behavior.

### Threat, Competition, and Group Position

Anti-immigrant attitudes are often explained through perceived economic threat, cultural threat, status threat, or group-position concerns. This matters for prompt design because threat cues may shift model outputs even when the identity label is unchanged.

Key readings:
- Blumer (1958), group position theory.
- Esses et al. (1998), instrumental model of group conflict.
- Brader et al. (2008), anxiety, group cues, and immigration threat.
- Sniderman et al. (2004), situational triggers and immigrant minorities.
- Hainmueller and Hopkins (2014), public attitudes toward immigration.

### Dehumanization

Migration discourse often dehumanizes through metaphors of floods, waves, invasions, contamination, animals, or faceless masses. LLM work should measure these separately from generic toxicity because dehumanization can be subtle and policy-relevant.

Key readings:
- Haslam (2006), dehumanization review.
- Esses et al. (2013), media, threat, and dehumanization of immigrants and refugees.

### Framing and Media Effects

Framing is about selection and salience: what aspects of an issue are emphasized, omitted, or made causally important. In LLM and IR systems, framing can appear through generated summaries, source ranking, citations, query expansion, and answer structure.

Key readings:
- Entman (1993), framing.
- Scheufele (1999), framing as media effects.
- Boomgaarden and Vliegenthart (2009), news content and anti-immigration attitudes.
- Eberl et al. (2018), European immigration media discourse review.

### Illegality and Legal Violence

Terms like "illegal immigrant" are not neutral labels; they are tied to legal, political, and institutional production of vulnerability. This is critical when evaluating LLM outputs about immigration law, asylum, deportation, and border control.

Key readings:
- De Genova (2002), migrant illegality and deportability.
- Menjivar and Abrego (2012), legal violence.

## How This Changes Our LLM Course

- Bias is not only stereotype polarity; it is also warmth/competence positioning, threat framing, dehumanization, and group boundary-making.
- Migration prompts should vary context cues: economic scarcity, crime, legality, humanitarian need, family ties, occupation, language, and local setting.
- Evaluation should separate sentiment, toxicity, dehumanization, deservingness, threat, agency, and legality.
- IR audits should examine frame exposure: security/criminality frames vs humanitarian/legal-rights/economic-contribution frames.
- Social-science theories can guide benchmark construction instead of relying only on demographic word lists.
