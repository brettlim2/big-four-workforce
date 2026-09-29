# Big-four workforce public dashboard

Static aggregate dashboard for ANZ / CBA / NAB / Westpac LinkedIn workforce signals joined to APRA, ABS, and TEQSA public data.

**Live page:** https://brettlim2.github.io/big-four-workforce/

No person-level data is published. Charts and tables are built from `data/dashboard.json`.

## Reading order

1. **Executive readout** — selected-bank headline, three KPIs, technology-share hero with Wilson intervals
2. **Three findings** — operating-model gap, location concentration, talent-flow advantage
3. **Six investigation modules** — function mix, talent flows, career paths, branch-to-digital, geography, education
4. **Evidence drawer** — defensibility ranking, method, sources, supported headlines

Use the bank / function / geography / period controls to explore; the default story is curated around CBA.

## Guardrails

- Counts are **observed profiles / signals**, not a workforce census
- Profiles per branch are a **footprint-density proxy**, not productivity
- Current-role start years are **normalized within each bank’s sample**
- Wilson intervals measure precision; they do not remove LinkedIn selection bias

## Defensibility ranking (this release)

| Rank | Workstream | Score | Tier |
| ---: | --- | ---: | --- |
| 1 | Stakeholder decision products (filtered claims) | 100.0 | high |
| 2 | Function mix and org design proxies | 91.5 | high |
| 3 | APRA / ABS public overlays | 86.1 | high |
| 4 | Employer transition network | 63.7 | medium |
| 5 | Career paths and CBA attractors | 40.6 | low |

Primary analyses to trust for public claims: **function mix**, **public overlays**, and **inter-bank network edges with large n**. Career-path transition cells are often sparse.

## Local rebuild

```bash
# on the analysis VM after normalize + insights
.venv/bin/python -m analysis deep
# then locally
bash scripts/build_dashboard.sh
```

GitHub Pages serves the site root from `main`.
