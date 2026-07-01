<h1 align="center">Perspectives on Gender Sensitization</h1>
<p align="center">A Kanpur-Based Quantitative Study · Full Analytics Lifecycle</p>

<p align="center">
  <img src="https://img.shields.io/badge/status-completed-lightgrey" alt="status"/>
  <img src="https://img.shields.io/badge/sample%20size-n%3D100-lightgrey" alt="sample"/>
  <img src="https://img.shields.io/badge/synthetic%20dataset-1%2C000%20rows-lightgrey" alt="synthetic"/>
  <img src="https://img.shields.io/badge/Python-3.9%2B-lightgrey" alt="python"/>
  <img src="https://img.shields.io/badge/license-CC%20BY--NC%204.0-lightgrey" alt="license"/>
</p>

<p align="center">
  <a href="docs/executive_summary.md">Executive Summary</a> ·
  <a href="docs/dashboard_spec.md">Dashboard Spec</a> ·
  <a href="docs/architecture.md">Architecture</a> ·
  <a href="#quick-start">Quick Start</a>
</p>

---

## What this is

A quantitative social research project measuring gender sensitization awareness among 100 young respondents (18–35) in Kanpur, India — restructured here as an **end-to-end data analytics case study**. Covers survey design → primary data collection → cleaning → exploratory and statistical analysis → visualization → key findings.

> **Original academic work:** MA Political Science dissertation, Christ Church College, Kanpur (CSJM University), 2023–24.
> **Supervisor:** Vibha Dikshit, Associate Professor, Department of Political Science.

---

## Highlights

| | |
|---|---|
| **70% sensitization rate** | ~70% of sampled Kanpur youth hold non-stereotypical gender attitudes |
| **60% training gap** | 60% have never received formal gender-sensitization training |
| **33 visualizations** | Chart-by-chart breakdown of every survey question plus thematic infographics |
| **1,000-row synthetic dataset** | Statistically mirrors published findings; reproducible via a seeded generator script |
| **Three-notebook pipeline** | Data cleaning → EDA → statistical analysis, in order |
| **Six thematic dimensions** | Awareness · Stereotypes · Roles · Equality · GBV · Demographics |

---

## Key findings

**Awareness**
- 77% had heard the term "gender sensitization" — but only ~39% could correctly define gender as a social construct (knowledge–vocabulary gap)
- 60% had never received any formal gender training

**Stereotypes & Roles**
- 82% agreed it is acceptable for men to cry — strong rejection of toxic-masculinity norms
- 75% disagreed that "men are strong, women are weak"
- 94% supported equal division of household chores when both partners work

**Equality & GBV**
- 91% supported equal pay for equal work
- 70% rejected the idea that women should tolerate violence to preserve a family
- 63% believed gender-sensitization training reduces incidents of gender-based violence

**Headline result:** youth are fairly sensitized, but institutional training is largely missing. The fastest policy lever is structured curriculum and workplace programs — not attitude campaigns.

Full write-up: [`docs/key_findings.md`](docs/key_findings.md) · [`docs/executive_summary.md`](docs/executive_summary.md)

---

## Methodology

| Component | Detail |
|---|---|
| Research type | Quantitative · descriptive |
| Instrument | Closed-ended Google Form |
| Sample size | 100 respondents |
| Sampling | Convenience + gender-stratified |
| Target population | Youth aged 18–35, Kanpur |
| Analysis | Frequency distribution · percentage analysis |
| Demographics | 86% aged 18–25 · 53% male / 47% female · 66% graduates |

*LGBTQIA+ respondents were not represented — acknowledged as a key limitation.*

Full details: [`docs/methodology.md`](docs/methodology.md) · Survey instrument: [`docs/questionnaire.md`](docs/questionnaire.md)

---

## Quick start

### Prerequisites
- Python ≥ 3.9
- Jupyter (for running the analysis notebooks)

### Installation

```bash
git clone https://github.com/anshikagknp/gender-sensitization-survey-analysis.git
cd gender-sensitization-survey-analysis

python -m venv .venv
source .venv/bin/activate          # macOS / Linux
# .venv\Scripts\activate           # Windows

pip install -r requirements.txt
```

### Run the analysis notebooks

```bash
jupyter lab
# Open analysis/ and run in order:
# 1. Data_Cleaning.ipynb
# 2. EDA.ipynb
# 3. Statistical_Analysis.ipynb
```

### Regenerate the synthetic dataset

```bash
python data/generate_dataset.py
# Outputs: data/synthetic_survey.csv (deterministic, seeded)
```

---

## Repository structure

```
gender-sensitization-survey-analysis/
│
├── data/
│   ├── generate_dataset.py     # Synthetic data generator (seeded, deterministic)
│   └── synthetic_survey.csv    # 1,000-row simulated dataset
│
├── analysis/
│   ├── Data_Cleaning.ipynb
│   ├── EDA.ipynb
│   └── Statistical_Analysis.ipynb
│
├── visualizations/             # 33 chart & infographic PNGs
│
├── docs/
│   ├── methodology.md
│   ├── questionnaire.md
│   ├── key_findings.md
│   ├── executive_summary.md
│   ├── architecture.md         # Project architecture & data flow
│   ├── dashboard_spec.md       # Dashboard design spec
│   └── research_paper_portfolio.pdf
│
├── requirements.txt
├── CITATION.cff
└── LICENSE
```

---

## Tech stack

<p>
  <img src="https://img.shields.io/badge/Google%20Forms-survey-lightgrey" alt="forms"/>
  <img src="https://img.shields.io/badge/Python-pandas%20%7C%20matplotlib-lightgrey" alt="python"/>
  <img src="https://img.shields.io/badge/Jupyter-notebooks-lightgrey" alt="jupyter"/>
</p>

---

## Ethical considerations

- All 100 responses were collected with informed consent via an anonymous Google Form. No PII was ever collected.
- The original response sheet has been permanently lost. Only published aggregate findings are represented here.
- The 1,000-row synthetic dataset is clearly labelled as simulated and must not be cited as primary research evidence.

---

## Citation

```bibtex
@misc{gupta2024gendersensitization,
  author    = {Gupta, Anshika},
  title     = {Perspectives on Gender Sensitization: A Kanpur-Based Quantitative Study},
  year      = {2024},
  publisher = {GitHub},
  url       = {https://github.com/anshikagknp/gender-sensitization-survey-analysis}
}
```

See [`CITATION.cff`](CITATION.cff) for the full machine-readable citation.

---

## Acknowledgements

- **Supervisor:** Vibha Dikshit, Associate Professor, Department of Political Science, Christ Church College, Kanpur
- Original literature review drew on 30+ academic sources on gender sensitization policy in India

---

## License

| Content | License |
|---|---|
| Findings, documentation, write-up | [CC BY-NC 4.0](LICENSE) |
| Code and scripts | MIT |

---

## Author

**Anshika Gupta** — MA Political Science, Christ Church College, Kanpur (CSJM University)
GitHub: [@anshikagknp](https://github.com/anshikagknp)
