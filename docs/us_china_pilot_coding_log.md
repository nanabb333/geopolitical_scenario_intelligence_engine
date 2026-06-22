# US-China Strategic Competition Pilot Coding Log

This log documents inclusion rationale, evidence basis, coding notes, and limitations for `data/us_china_strategic_competition_pilot.csv`.

## V2P001

- Event ID: V2P001
- Event Name: CHIPS and Science Act signed
- Category: Industrial Policy
- Why Included: Anchor US industrial-policy event linked to semiconductor capacity and strategic competition.
- Evidence Basis: White House signing remarks dated 2022-08-09.
- Coding Notes: Included as broad industrial policy rather than a firm-specific event.
- Ambiguity or Limitation: Highly anticipated legislation; not suitable for simple event-day interpretation without caveats.

## V2P002

- Event ID: V2P002
- Event Name: BIS advanced computing and semiconductor manufacturing export controls
- Category: Export Controls
- Why Included: Core US-China technology restriction event that extends current V1 export-control coverage.
- Evidence Basis: Federal Register rule associated with October 2022 BIS controls.
- Coding Notes: Event date uses rule announcement date.
- Ambiguity or Limitation: Rule includes multiple product categories and technical provisions.

## V2P003

- Event ID: V2P003
- Event Name: YMTC and other Chinese entities added to Entity List
- Category: Sanctions / Entity List
- Why Included: Named-entity technology restriction involving Chinese semiconductor firms.
- Evidence Basis: Federal Register entity-list additions.
- Coding Notes: Coded as sanctions/entity-list rather than broad export controls.
- Ambiguity or Limitation: Entity-list actions are legal restrictions but not identical to financial sanctions.

## V2P004

- Event ID: V2P004
- Event Name: Japan announces semiconductor-equipment export-control plan
- Category: Export Controls
- Why Included: Allied technology-control alignment relevant to US-China strategic competition.
- Evidence Basis: Japan METI press release dated 2023-03-31.
- Coding Notes: Geography is Japan/China because the initiating actor is Japan.
- Ambiguity or Limitation: Not a direct US action; compare cautiously with US-origin controls.

## V2P005

- Event ID: V2P005
- Event Name: China restricts Micron products in critical information infrastructure procurement
- Category: Sanctions / Entity List
- Why Included: China-side named-company restriction and retaliation/procurement-risk channel.
- Evidence Basis: Cyberspace Administration of China notice dated 2023-05-21.
- Coding Notes: Coded as procurement restriction rather than financial sanction.
- Ambiguity or Limitation: Exposure depends on implementation and China revenue dependence.

## V2P006

- Event ID: V2P006
- Event Name: China announces gallium and germanium export controls
- Category: Critical Minerals
- Why Included: Critical-minerals restriction adjacent to semiconductor, defense, and clean-energy supply chains.
- Evidence Basis: China Ministry of Commerce notice dated 2023-07-03.
- Coding Notes: Broad sector-wide event with multiple downstream channels.
- Ambiguity or Limitation: Market relevance depends on licensing and firm-level material exposure.

## V2P007

- Event ID: V2P007
- Event Name: US executive order on outbound investment in sensitive technologies
- Category: Strategic Investment Screening
- Why Included: Anchor event for outbound investment screening in strategic technology sectors.
- Evidence Basis: White House executive order dated 2023-08-09.
- Coding Notes: Framework event related to semiconductors, microelectronics, AI, and quantum.
- Ambiguity or Limitation: Implementation details require separate final-rule coding.

## V2P008

- Event ID: V2P008
- Event Name: BIS updates advanced computing and semiconductor export controls
- Category: AI Chip Restrictions
- Why Included: Key AI-chip restriction update and direct extension of 2022 controls.
- Evidence Basis: Federal Register rule published after October 2023 BIS update.
- Coding Notes: Named companies are listed as impacted because AI accelerator exposure is explicit in market context.
- Ambiguity or Limitation: The row does not imply an expected direction or investment conclusion.

## V2P009

- Event ID: V2P009
- Event Name: China announces graphite export controls
- Category: Critical Minerals
- Why Included: Critical-minerals event connecting US-China competition to battery and strategic supply chains.
- Evidence Basis: China Ministry of Commerce notice dated 2023-10-20.
- Coding Notes: Less semiconductor-adjacent than gallium/germanium but relevant to supply-chain risk.
- Ambiguity or Limitation: Sector impact is broader than technology hardware.

## V2P010

- Event ID: V2P010
- Event Name: China restricts export of rare-earth processing technology
- Category: Critical Minerals
- Why Included: Strategic minerals technology-control event relevant to broader US-China competition.
- Evidence Basis: Reuters report dated 2023-12-21.
- Coding Notes: Included with medium date confidence pending official-catalog normalization.
- Ambiguity or Limitation: Should be reviewed against official catalog sources before production use.

## V2P011

- Event ID: V2P011
- Event Name: TSMC Arizona CHIPS preliminary terms announced
- Category: Supply Chain Relocation
- Why Included: State-backed relocation and domestic advanced semiconductor capacity example.
- Evidence Basis: US Commerce Department announcement dated 2024-04-08.
- Coding Notes: Coded as supply-chain relocation rather than only industrial policy.
- Ambiguity or Limitation: Preliminary terms are firm-specific and should not represent all relocation activity.

## V2P012

- Event ID: V2P012
- Event Name: China semiconductor Big Fund III registered
- Category: Industrial Policy
- Why Included: China-side industrial-policy counterpart to US semiconductor support.
- Evidence Basis: Reuters report on fund registration dated 2024-05-27.
- Coding Notes: Event date uses reported registration date of 2024-05-24.
- Ambiguity or Limitation: Official registration should be reviewed before production coding.

## V2P013

- Event ID: V2P013
- Event Name: China launches Taiwan-related military drills after inauguration period
- Category: US-China Strategic Competition Pilot Dataset
- Why Included: Taiwan-related tension included as one subcategory in the broader US-China pilot.
- Evidence Basis: Reuters report dated 2024-05-23.
- Coding Notes: Coded under pilot umbrella with subcategory `taiwan_related_tension`.
- Ambiguity or Limitation: Does not make the pilot Taiwan-focused and does not include market-return evidence.

## V2P014

- Event ID: V2P014
- Event Name: US Treasury finalizes outbound investment rule for China-related technologies
- Category: Strategic Investment Screening
- Why Included: Final implementation event for outbound investment screening.
- Evidence Basis: US Treasury press release dated 2024-10-28.
- Coding Notes: Related to V2P007 but materially distinct as final rule implementation.
- Ambiguity or Limitation: Potential duplicate relationship should be tracked in later schema use.

## V2P015

- Event ID: V2P015
- Event Name: BIS announces controls on advanced computing and semiconductor manufacturing items including HBM
- Category: AI Chip Restrictions
- Why Included: Later AI-chip and semiconductor-manufacturing control event relevant to V2 expansion.
- Evidence Basis: BIS press release dated 2024-12-02.
- Coding Notes: Included for schema coverage; not wired into V1 workflow.
- Ambiguity or Limitation: Final rule text should be checked before production scoring or retrieval use.
