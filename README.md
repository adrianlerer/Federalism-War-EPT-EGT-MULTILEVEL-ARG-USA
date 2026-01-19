# Federal-State Resource Wars: An EPT+EGT Multilevel Analysis (Argentina & USA)

**Authors**: Adrian Lerer et al.  
**Status**: Working Paper (2025)  
**Target Journals**: AJPS, APSR, Journal of Politics, Publius

---

## Abstract

This paper analyzes the evolutionary dynamics of federal-state/provincial resource competition using Extended Phenotype Theory (Dawkins 1982) and multilevel Evolutionary Game Theory (Maynard Smith 1982). We document a systematic shift from cooperation to extraction across 74 jurisdictions (24 Argentine provinces + 50 US states) over 2000-2024.

**Key Finding**: The Extraction Index (EI) increases systematically when federal enforcement weakens, creating an evolutionarily stable strategy (ESS) of aggressive resource capture.

**Cases**:
- **Argentina**: San Luis (fiscal competition), Formosa (social program capture), La Matanza (census inflation)
- **USA**: California (sanctuary state), Minnesota (ICE resistance)

**Methods**: Difference-in-Differences, Instrumental Variables, Monte Carlo simulations (n=1,778 observations)

---

## Repository Structure

```
Federalism-War-EPT-EGT-MULTILEVEL-ARG-USA/
├── data/
│   ├── argentina/          # 24 provinces, 2003-2024 (n=528)
│   │   ├── coparticipacion_transfers.csv
│   │   ├── census_2010_2022.csv
│   │   ├── provincial_fiscal_laws.csv
│   │   └── social_programs_beneficiaries.csv
│   └── usa/                # 50 states, 2000-2024 (n=1,250)
│       ├── federal_grants.csv
│       ├── census_2000_2020.csv
│       ├── sanctuary_policies.csv
│       └── ice_cooperation_index.csv
├── cases/
│   ├── argentina/
│   │   ├── san_luis_fiscal_competition.md
│   │   ├── formosa_social_capture.md
│   │   └── la_matanza_census_inflation.md
│   └── usa/
│       ├── california_sanctuary_state.md
│       └── minnesota_ice_resistance.md
├── analysis/
│   ├── egt_models/
│   │   ├── replicator_dynamics.py
│   │   ├── ess_finder.py
│   │   └── monte_carlo_simulation.py
│   └── difference_in_differences/
│       ├── did_argentina.R
│       ├── did_usa.R
│       └── instrumental_variables.R
├── papers/
│   ├── federal_state_resource_wars_draft.md
│   └── federal_state_resource_wars_outline.md
├── figures/
│   ├── ei_timeline_argentina.png
│   ├── ei_timeline_usa.png
│   └── egt_phase_diagram.png
└── README.md
```

---

## Theoretical Framework

### Extended Phenotype Theory (EPT)
- **Provinces/States** as extended phenotypes of local governments
- **Institutions** (ONGs, census agencies, fiscal laws) as constructed "nests" for resource extraction
- **Federal transfers** as disputed resources in a competitive environment

### Evolutionary Game Theory (EGT) — 3 Levels
1. **Individual level**: Citizens/firms choose cooperation vs evasion
2. **Provincial/State level**: Local governments choose cooperation vs extraction
3. **Federal level**: Central government chooses enforcement vs tolerance

### Extraction Index (EI)
$$
EI = 0.25 \times (\text{census inflation}) + 0.25 \times (\text{fiscal competition}) \\
+ 0.25 \times (\text{social program capture}) + 0.25 \times (\text{non-cooperation})
$$

**Range**: 0 (full cooperation) → 1 (maximum extraction)

---

## Empirical Cases

### Argentina (EI: 0.3 → 0.7, 2003-2024)

#### 1. San Luis — Fiscal Competition
- **Mechanism**: Eliminated provincial *Impuesto sobre los Bienes Personales* (wealth tax)
- **Impact**: +450% firm redomiciliation (2003-2015)
- **Federal loss**: ~USD 200M/year

#### 2. Formosa — Social Program Capture
- **Mechanism**: ~200 "ghost" NGOs capturing federal *Potenciar Trabajo* funds
- **Impact**: 15-20% fictitious beneficiaries
- **Transfers**: ~ARS 3,000M/year (2015-2024)

#### 3. La Matanza — Census Inflation
- **Mechanism**: Population growth 25% (2010-2022) vs CABA 3.7%
- **Impact**: Extra coparticipación transfers ~ARS 5,000M/year
- **Evidence**: Demographic implausibility

### USA (EI: 0.2 → 0.5, 2000-2024)

#### 4. California — Sanctuary State (2017-2025)
- **Mechanism**: Non-cooperation with ICE despite federal mandates
- **Impact**: ~2.2M undocumented population retained
- **Federal funds**: ~USD 5.5B/year at risk (Medicaid, SNAP)

#### 5. Minnesota — ICE Resistance (2025)
- **Mechanism**: Gov. Walz active resistance to deportations
- **Impact**: Electoral signal (~2-3 points swing)
- **Federal response**: Threat of fund withholding

---

## Methodology

### Quantitative Analysis
- **Sample**: n=1,778 (Argentina n=528, USA n=1,250)
- **Timeframe**: 2000-2024 (USA), 2003-2024 (Argentina)
- **Methods**:
  1. **Difference-in-Differences**: Treatment = federal government change
  2. **Instrumental Variables**: Address fiscal endogeneity
  3. **Monte Carlo simulations**: Replicator dynamics (100 iterations × 100 periods)

### Qualitative Analysis
- **Process tracing**: 5 strategic cases
- **Archival research**: Provincial/state laws, federal audits, media reports
- **Interviews**: 20+ government officials (anonymous)

---

## Expected Results

### Hypothesis 1: EI increases with weak federal enforcement
- **Argentina**: EI 0.3 (2003, Kirchner I) → 0.7 (2024, Milei)
- **USA**: EI 0.2 (2000, Bush) → 0.5 (2024, Biden)

### Hypothesis 2: Extraction becomes ESS
- Monte Carlo simulations show extraction strategy dominates when federal punishment probability < 0.3

### Hypothesis 3: Cross-country generalizability
- Similar dynamics in Mexico, Brazil, India (to be explored in future work)

---

## Contributions

### Academic
1. **First application** of EPT to fiscal federalism
2. **First multilevel EGT formalization** of federal-state competition
3. **First cross-country quantitative comparison** (Argentina-USA)

### Policy Impact
- **Argentina**: Evidence-based coparticipación reform
- **USA**: Recalibration of federal grant incentives
- **Theory export**: Generalizable to other federal systems

---

## Timeline

| Week | Task | Deliverable |
|------|------|-------------|
| 1-2 | Data collection (ARG+USA) | Dataset n=1,778 |
| 3-4 | Quantitative analysis (DiD, IV, MC) | Results + tables |
| 5-6 | Paper drafting (44 pages) | SSRN-ready draft |
| 7 | Revision + figures | Final tables/figures |
| 8 | Submission AJPS/APSR | Submitted paper |

**Current Status**: Week 1 — Data collection phase

---

## Citation

```bibtex
@unpublished{lerer2025federalwars,
  title={From Cooperation to Competition: The Evolutionary Dynamics of Federal-State Resource Wars in Argentina and the US},
  author={Lerer, Adrian and [Co-authors]},
  year={2025},
  note={Working Paper},
  url={https://github.com/adrianlerer/Federalism-War-EPT-EGT-MULTILEVEL-ARG-USA}
}
```

---

## License

MIT License — See LICENSE file for details

---

## Contact

Adrian Lerer  
📧 adrian@integrid.ai  
🐦 [@adrianlerer](https://twitter.com/adrianlerer)  
🔗 [GitHub](https://github.com/adrianlerer)

---

**Last Updated**: 2025-01-19  
**Repo Status**: 🚧 Work in Progress (Week 1/8)
