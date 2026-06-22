# V2 Dataset Readiness Assessment

## Whether the Current Workflow Can Support Broader Datasets

The current V1 workflow can support broader datasets at the architecture level.

The workflow already separates:

- scenario intake;
- classification;
- historical analogue retrieval;
- market-reaction comparison;
- observed pathway generation;
- executive memo generation;
- Markdown export.

These stages are not inherently semiconductor-only. The limiting factor is the current dataset and controlled vocabulary, not the overall workflow design.

Broader datasets can be introduced if future events preserve structured fields for category, subcategory, geography, sector, strategic significance, market relevance, source quality, and coding notes.

## Risks of Expansion

- Category drift: new categories may be coded inconsistently without a dictionary.
- Overclaiming: broader examples may imply support before enough events exist.
- Sparse market data: many geopolitical events will lack clean event-firm return rows.
- Ambiguous event dates: military, cyber, shipping, and sanctions events may unfold over multiple dates.
- Duplicates: announcement, enforcement, retaliation, and market-reaction dates can be confused.
- Retrieval mismatch: current classification and scoring logic may not fully exploit future V2 fields until a later code sprint.
- Documentation burden: broader coverage requires stronger source and coding discipline.

## Expected Challenges

- Defining event boundaries for multi-day crises.
- Separating direct events from background geopolitical tension.
- Assigning geography when events have global or supply-chain effects.
- Coding affected companies without drifting into investment recommendations.
- Distinguishing sanctions, export controls, procurement bans, and industrial policy.
- Maintaining deterministic rules while expanding vocabulary.
- Preventing example questions from outpacing actual coded data coverage.

## Recommended First Expansion Direction

Recommended first expansion direction: US-China Strategic Competition Pilot Dataset.

Reasoning:

- It connects naturally to the current semiconductor validation dataset.
- It is broader and more recruiter-recognizable than a Taiwan-first framing.
- It connects semiconductors, trade, sanctions, supply chains, AI infrastructure, critical minerals, investment screening, and geopolitical risk.
- It tests whether the workflow handles multiple strategic-competition mechanisms without requiring new product features.
- It preserves Taiwan-related tension as an important subcategory without making Taiwan the central product narrative.
- It has stronger risk analytics relevance across technology, industrials, logistics, defense, critical minerals, and regional exposure.

Recommended pilot scope:

- 30-45 candidate events across US-China strategic competition.
- Include export controls, sanctions, AI chip restrictions, semiconductor industrial policy, entity-list actions, critical minerals, supply-chain relocation, strategic investment screening, and Taiwan-related tension as one subcategory.
- Code event-date confidence carefully, especially for sanctions implementation, investment-screening decisions, and multi-stage policy actions.
- Keep Taiwan-related events distinct from semiconductor-policy events unless the source directly links them.
- Add market rows only where event dates and affected assets are defensible.

Second recommended expansion direction: targeted category deepening after the US-China pilot.

Reasoning:

- After a US-China pilot, the strongest next deepening areas are shipping and maritime disruption, energy security, cyber operations, and defense industrial policy.
- These categories should be added after the pilot clarifies whether schema changes or workflow logic changes are necessary.
- This sequencing avoids overclaiming broad coverage before the dataset exists.

## Readiness Verdict

V2 dataset expansion is ready for schema-design and pilot-coding preparation.

The repository should not expand source logic until a pilot dataset exposes a concrete need. The next sprint should focus on coding standards, event templates, category dictionary use, and a small reviewed candidate-event set.
