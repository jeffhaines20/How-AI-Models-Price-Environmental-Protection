# Handoff: AI Environmental Tradeoffs Study

Nov 13, 2026

Paste or attach this brief at the start of a new Claude chat to continue the project. The full research protocol is here: https://claude.ai/code/artifact/6eeeebdf-4e59-42b8-b8e4-f435eb0247f0

## Background

- I'm the AI program director at Keiser University, based in central Florida.
- I may be paired with a research advisor whose interests are public health, climate change, and the politics and governance of environmental issues. I'm looking for a project that fits his interests and is still clearly about AI.
- We first explored AI governance topics broadly. Then we looked at the environmental side of AI: data center energy and water policy, public health costs of data center air pollution, and AI for climate-health early warning.
- I settled on my own idea: **measuring how AI models trade off environmental protection against economic growth**. Officials and staffers increasingly use AI for policy research and recommendations, so these implicit tradeoffs matter.

## The study

**Question:** What implicit prices do LLMs put on environmental and health harms compared with economic benefits when advising on real policy decisions, and do those prices shift depending on who is asking?

**Design decisions so far:**

- **Conjoint vignette experiment.** Models recommend approve or deny on permitting and siting decisions. Examples include a data center with gas turbines, mining near wetlands, relaxing emissions standards, groundwater permits, and coastal development.
- **Randomized attributes.** Jobs, tax revenue, investment, premature deaths, asthma cases, CO2, wetland acres, water withdrawal, distribution of the health burden, and local opinion.
- **Decisions, not attitude questions.** Implied prices come from coefficient ratios in a conditional logit, plus AMCEs. This avoids the numeracy problems that direct willingness-to-pay questions run into.
- **Benchmarks.** EPA's value of a statistical life and social cost of carbon, plus a matched human survey sample, and possibly government staff.
- **Sycophancy arm.** First-person user identities: Republican and Democratic staffers, environmental agency analyst, economic development official, health department official. Framing factors are crossed with identity.
- **Open-ended memo arm.** Free-text briefing memos, coded for omitted considerations, decisive factors, hedging, and environmental justice.
- **Models.** 8–12 current models (U.S. developers plus one Chinese and one European model), reasoning and non-reasoning modes, default temperature, 10–20 runs per cell, with versions logged.
- **Robustness.** Three paraphrases per scenario, comprehension checks, refusals treated as an outcome, a second-wave drift rerun, and OSF pre-registration.
- **Timeline.** About 12 months. The main cost is API credits.

## Prior work found

- [Kunkel et al. 2026, "Greener Than Humans?"](https://arxiv.org/html/2606.02741v1), from the German Environment Agency and GFZ. This is the closest study. It surveyed 31 models with German environmental-attitude items and found models more environmentally progressive than the public. Most priced CO2 at 50–200 euros, against an agency estimate of 300. Claude Sonnet 4.6 was the second most sycophantic of the three models tested. Its limits are that it measured attitudes rather than decisions, its WTP answers were unreliable, and it used a German context.
- [Conjoint study of LLM economic policy choices (2025)](https://arxiv.org/pdf/2507.15771) and [LLM military intervention choices (2025)](https://arxiv.org/pdf/2507.06277). These provide a method template but have no environmental attributes.
- [Biased LLMs can influence political decision-making (ACL 2025)](https://aclanthology.org/2025.acl-long.328.pdf). This shows biased models shift human budget decisions, which supports the stakes.

## Status and next steps

**Done:** a full research protocol doc (linked at the top) and a pitch paragraph for the potential advisor.

**Open questions:**

- [ ] Should the human benchmark be the general public, government staff, or both?
- [ ] Should the scenarios lean toward health (air quality) or climate (CO2)?
- [ ] Calibrate attribute levels against real permit filings and health-impact studies
- [ ] Pick the exact model list and estimate API cost
- [ ] Get the advisor's reaction and adjust scope

**How to resume:** Start the new chat with something like: "Here's a handoff brief for a research project I'm developing. Read it and the linked protocol doc, then help me with [next task]."
