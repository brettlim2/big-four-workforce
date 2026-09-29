# Big-four workforce public dashboard

Static aggregate dashboard for ANZ / CBA / NAB / Westpac LinkedIn workforce signals joined to APRA, ABS, and TEQSA public data.

**Live page:** https://brettlim2.github.io/big-four-workforce/

No person-level data is published. Charts and tables are built from `docs/data/dashboard.json`.

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

GitHub Pages serves the `docs/` folder from `main`.
