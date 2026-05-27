# Texas TDLR Contractor Bond Compliance — May 2026

**46.9% of Texas apprentice electricians have expired surety bonds.** Across all TDLR-regulated trades, 29.3% of licensees are currently non-compliant with state bonding requirements.

This repository contains the dataset behind the findings at **[quantumsurety.bond/bond-compliance-by-trade](https://quantumsurety.bond/bond-compliance-by-trade)**.

## Key Findings

| Stat | Value |
|------|-------|
| Total TDLR licensees analyzed | 816,438 |
| Licensees with expired bonds | ~239,000 (29.3%) |
| Apprentice Electricians — expired rate | **46.9%** (93,509 / 199,435) |
| Consent Tow Truck Operators — expired rate | **44.8%** (2,724 / 6,082) |
| A/C Technicians — expired rate | **38.9%** (15,195 / 39,040) |

## Files

- `compliance_by_trade.csv` — Bond compliance rates for all 22 TDLR license types (May 2026)
- `methodology.md` — Data collection and calculation methodology

## Live Tools

- **[Texas Bond Watch](https://quantumsurety.bond/texas-bond-watch)** — Live county-level tracker, search any contractor
- **[Compliance by Trade](https://quantumsurety.bond/bond-compliance-by-trade)** — A–F graded breakdown of all 22 TDLR license types
- **[Free API](https://verify.quantumsurety.bond/api-docs.html)** — `/api/contractor/lookup/:license` — no auth, CORS-enabled
- **[Verify Tool](https://verify.quantumsurety.bond)** — Search 558K+ TX notaries + 816K+ contractors

## Why This Matters

A surety bond is the consumer protection mechanism for licensed contractor work in Texas. When a contractor causes damage, the bond is what a homeowner can file a claim against. An expired bond means that protection is gone — even if the contractor still has a valid license number.

TDLR requires all licensed contractors to maintain active surety bonds as a condition of licensure. The data shows widespread non-compliance, particularly among apprentice electricians (46.9%) and A/C technicians (38.9%).

## Data Source

**Texas Department of Licensing and Regulation (TDLR)** public licensing dataset  
Available at: [data.texas.gov](https://data.texas.gov/dataset/TDLR-Licensees/7358-krk7) (dataset ID: 7358-krk7)  
Data accessed: May 2026  
Updated: Monthly

## Contact

Theodore Sparks  
Quantum Surety LLC — TDI License #3480229  
contact@quantumsurety.bond | (214) 666-8718  
[quantumsurety.bond](https://quantumsurety.bond) | [Press Kit](https://quantumsurety.bond/press)

_Data analysis and live verification tool built by Quantum Surety LLC. All source data is public record from TDLR._
