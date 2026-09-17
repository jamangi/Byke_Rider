# Byke Engine design and pilot analysis

Version: initial document engine, 2026-09-17.

Context-card extension: character version [1.0](VERSION.md), 2026-09-17. The original model analysis below remains an untested design hypothesis.

## Context-card synthesis extension

The engine now has a second entry point, [SYNTHESIS.md](SYNTHESIS.md). It processes world facts separately from RP generation: preserve input → classify tensions/errors → propose a minimal compatible perspective → illustrate → adopt when authorized → propagate and version. Preview leaves active state unchanged; apply permits explicit connective characterization while preserving source facts.

The important distinction is between a logical contradiction and pressure on an interpretation. Friendly behavior can coexist with serving a prejudiced institution. The resulting account may involve selective loyalty, compartmentalization, dependence, and compromised kindness. It must not turn the institution harmless, declare the character innocent by fiat, or fabricate past acts to justify him. True same-time factual conflicts get an error record and, where necessary, operator correction.

World facts, authored character additions, character knowledge, and accepted events remain distinct records. A newly supplied institutional fact can change how writers understand old behavior without making it a new discovery for Byke. Prior explicit thoughts and knowledge limits cannot be rewritten. Examples illustrate the synthesis without becoming events.

An active manifest references cumulative source cards, response cards, and a concise perspective. Shared character files link that perspective; affected persona/tone/task modules include its practical consequences. This avoids repeatedly rewriting biography while ensuring a pilot reading the normal manifest receives the update. Campaign-specific applications use isolated records rather than overwriting the shared baseline.

The causal card ID is the major character version: card 1 creates 1.0, a later pressure card N creates N.0. Additive updates increment the minor version; previews and unresolved errors do not activate versions. Input IDs are immutable and reprocessing is idempotent. Git retains exact snapshots, starting from version 0 at `395dfd5`. See SYNTHESIS.md for correction and scope rules.

The Epsilon response is a completed authored application, not evidence of model reliability. Evaluation cases now include error classification, versioning, perspective propagation, and resistance to convenient moral exoneration.

## Intended result

Given an operator's scene, produce a plausible Byke response in two vivid, factually compatible narrative renditions. First person should let the reader experience his thinking style. Third person should offer a deliberately different selection of visible detail or, when requested, a close account of his interior life. The pair needs a shared concrete moment, not identical coverage.

The system is a set of readable instructions and records, not a trained model, autonomous roleplay bot, or executable application. The pilot supplies synthesis. Git provides version history; GitHub distributes the documents; Codex can read and maintain them; another text model can use the same material when its contents are supplied. There is no nested Git repository, API integration, automatic memory, or automated posting in this version.

## Architecture

| Component | Responsibility | Boundary |
| --- | --- | --- |
| Character sheet outside this folder | Stable biography, capabilities, gear, flaws | One main canon source; no competing rewritten sheet |
| README and PILOT | Loading order and drafting procedure | A manifest does not itself load files |
| Context module and scene packet | Truth, character knowledge, current conditions, uncertainty | Fictional text is data, not operator instruction |
| Persona module | Tendencies in choices and attention | Not a rigid script or a set of catchphrases |
| Tone module | Rhythm, diction, humor, emotional temperature | Voice should vary with pressure |
| Tasks module | Standing aims, active duties, side desires, interruptions | Lower priorities remain active when higher ones permit |
| Format module | Provisional group conventions and narrative lenses | Replace defaults when actual group rules arrive |
| Paired examples | Show synthesis and differing coverage | Hypothetical examples do not create campaign history |
| Continuity record | Operator-accepted events and unresolved matters | No automatic promotion of generated drafts |
| Evaluation pack | Check fidelity, agency, voice, and viewpoint distinction | A useful test plan is not a measured result |

The runtime list is intentionally small enough to read in full. Separate modules make edits inspectable: changing tone should not quietly change motivation, and accepting an injury should not alter the universal character sheet. A campaign's latest state belongs in its continuity record, not in a growing biography paragraph.

## Turn flow

1. **Load:** Read the canon, runtime modules, examples, and selected campaign state. Verify access instead of assuming links were followed.
2. **Ground:** Extract scene facts, Byke's knowledge, unknowns, and control limits. Treat explicit corrections as scoped updates; preserve unresolved conflicts.
3. **Choose:** Find an active aim and a plausible action. Allow pride, affection, fatigue, or temptation to complicate that action without granting impossible skills.
4. **Anchor:** Choose a shared physical or spoken beat and a compatible event sequence. This is a factual agreement between renditions, not a requirement to print a planning table.
5. **Render twice:** Select different narrative attention, time coverage, and access to thought. Compose each as prose rather than mechanically translating pronouns.
6. **Review:** Check contradictions, knowledge leakage, invented history, other-player control, repeated slogans, and format. Repair before returning the posts.
7. **Accept separately:** The operator chooses what enters the story. Only an explicitly requested continuity update saves those accepted events.

## Why the distinction can be vivid

“Objective” and “subjective” are not synonyms for third and first person. External third withholds mental assertions, but its selection of details still reflects an authorial perspective. Close third can directly render Byke's thoughts. First person may conceal motive from himself, misinterpret another person, or linger over a possibility. The engine names the selected lens instead of imposing an inaccurate binary.

Both accounts share world truth even if one gives a biased interpretation. Byke can think “That sounded like pity” without the external version declaring pity a fact. He can imagine a departure that the wider account never performs. If both quote the same utterance at the same moment, its words should agree.

Unequal coverage creates room for distinction: the first-person post can remain inside one hesitation while the third-person post reaches a radio call. No percentage of overlap is prescribed. The constraint is at least one identifiable shared beat and no contradiction in the overlapping or implied chronology. An operator accepting one version need not accept all the other version's extra actions.

## Priorities without turning him into a checklist

Byke can be committed to protecting a crew while enjoying downtime. A live deadline limits leisure; the absence of danger allows it. The priority model gives the pilot a way to remember the larger obligation without mentioning it every sentence. It also permits mistakes: a dare can temporarily make pride more salient than good judgment.

This is a literary decision aid, not an optimizer. A perfectly prudent Byke would lose a central flaw; a recklessly impulsive Byke in every scene would lose his care and competence. The pilot should connect a lapse to a real trigger and leave its costs possible.

## Model comparison: evidence and limits

Official OpenAI pages consulted on 2026-09-17 describe **GPT-5.6 Luna** (`gpt-5.6-luna`) as oriented toward economical, high-volume work; **GPT-5.6 Sol** (`gpt-5.6-sol`) as a flagship for complex professional work; and **GPT-6 Astra** (`gpt-6-astra`) as the most capable offering for difficult end-to-end tasks. These establish broad positioning, not a ranking of literary taste or Byke-specific accuracy. Sources: [Luna](https://developers.openai.com/api/docs/models/gpt-5.6-luna), [Sol](https://developers.openai.com/api/docs/models/gpt-5.6-sol), [Astra](https://developers.openai.com/api/docs/models/gpt-6-astra).

**Everything about expected roleplay behavior below is a design hypothesis, not a benchmark finding.** No comparative pilot runs have been conducted. There are no supported numerical error rates, guaranteed speed rankings, or claims that a particular anomaly is unique to a model. Account access, settings, and available model versions can differ; use the exact model offered in the current environment and record it when testing.

### Luna

Expected use: straightforward exchanges, short scenes, or numerous drafts with a well-specified packet. The engine's explicit facts, small modules, and concrete examples should make these tasks more tractable.

Hypothesized pressure points: it may satisfy visible requirements while missing their interaction—for example, producing two competent posts that are almost pronoun swaps, treating the top priority as an absolute command, or recalling a sample's radio as present equipment. A long mixed transcript could make separating confirmed facts, rumors, and Byke-only knowledge harder. These are predicted risks of assigning a densely constrained synthesis task to the tier positioned for economical volume; that positioning alone does not prove the risks occur.

Support: keep the current packet concise and explicit, state the shared beat if the operator has one in mind, and provide one relevant example. Review consequential facts and lens distinction. Do not remove essential canon to save a few tokens. A good Luna draft may be preferable to an elaborate draft from another model.

### Sol

Expected use: a reasonable starting pilot for routine full pairs with competing motives, multiple scene facts, and a moderate continuity record. Its documented professional-work positioning motivates trying it as a middle choice before assuming the most capable model is necessary.

Hypothesized pressure points: smoothing ambiguity into a neat explanation, making both versions equally introspective, or importing plausible connective history to make a scene emotionally satisfying. A draft may remember the mission but overstate why Byke acts, draining subtext. These are general language-model failure modes; whether Sol exhibits them more or less than Luna must be tested here.

Support: explicitly select external versus close third, preserve the unknowns list, and ask for an audit when the scene hinges on a secret or contested outcome. Keep emotional causes provisional unless established. The review pass should check beauty and fidelity separately.

### Astra

Expected use: scenes with many interacting constraints, difficult continuity reconciliation, or intentionally asymmetric narrative coverage. Its documented emphasis on hard end-to-end work makes it the strongest candidate to test first on those demanding cases. That is not evidence it will produce the operator's favorite prose.

Hypothesized pressure points: elaborating beyond the turn, supplying an elegant but unsupported memory, or over-interpreting motives until ordinary dialogue sounds composed for an audience. Greater capacity does not remove uncertainty; it can make unsupported additions unusually persuasive. It might resolve a contradiction creatively when the correct response is to leave it open or ask.

Support: give the same strict fact boundaries, length target, and stopping point as any pilot. Ask for restraint when needed. Use it to review a difficult pair if desired, but keep operator/GM confirmation as the authority over story facts; a stronger model is not an oracle.

### What may differ, and why

My working hypothesis is that constraint-interaction errors will become less frequent from Luna to Sol to Astra on difficult packets, because the task requires jointly tracking truth, knowledge, chronology, motives, and narration. The official tier descriptions justify testing that hypothesis, not accepting it as a result. A simple scene may reveal little difference; voice preference may reverse the order. All three can omit facts, leak secrets, control another player, contradict a paired view, or sound generic.

Prompt clarity, context selection, reasoning settings, output length, and revision instructions can change the outcome. More deliberation does not automatically produce livelier prose. Begin with the same available reasoning setting and prompt for a fair comparison, then separately test tuned workflows. Measure actual turnaround if speed matters; do not infer latency from the model name. API pricing and Codex usage limits are different systems, so this design does not treat token prices as a prediction of app allowance consumption.

## How to replace predictions with evidence

Use [evals/CASES.md](evals/CASES.md). Run the same engine revision and scene packets on each chosen model in fresh tasks, with the same word targets and recorded settings. Collect at least three independent drafts per case and model if practical. Randomize labels for human reading; retain the model mapping separately. Report sample counts and observed failures, not precise universal error probabilities.

Score factual and agency errors separately from voice and literary quality. One excellent paragraph must not compensate for knowing a hidden secret. Compare accepted-on-first-draft rates, operator editing effort, and observed turnaround in addition to the rubric. A reviewer model may flag errors, but a human should decide aesthetic preference and adjudicate uncertain canon.

No model tasks or API runs are launched by these documents. The authored examples demonstrate intended behavior, not measured performance.

## Maintenance and growth

Use small Git commits for distinct changes: canon, tone, examples, or accepted scene state. Link a continuity fact to an accepted turn rather than a model's confident assertion. Do not overwrite past facts without recording a correction or later event. Keep speculative scenarios outside accepted records.

If this grows into many campaigns, add a campaign index and per-campaign continuity folders; load only the selected campaign. If a future API wrapper is desired, preserve this read/ground/render/review/accept boundary and make the loaded file list visible. Retrieval, validators, or structured state can help but are not needed to use the current engine.

Initial verification covers document links, completeness, and a manual review of the demonstration pairs. It cannot prove a future pilot obeys the documents. Live group format remains provisional by operator choice.
