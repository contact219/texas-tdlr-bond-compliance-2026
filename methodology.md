# Methodology

## Data Source

The underlying data is the **Texas Department of Licensing and Regulation (TDLR) Licensees dataset**, a public record maintained by the State of Texas.

- **Source:** Texas Open Data Portal — [data.texas.gov, dataset ID 7358-krk7](https://data.texas.gov/dataset/TDLR-Licensees/7358-krk7)
- **Access method:** Socrata API (`https://data.texas.gov/api/views/7358-krk7/rows.csv`)
- **Dataset size:** ~816,000 records as of May 2026
- **Refresh cadence:** Monthly (Quantum Surety refreshes the 1st of each month)

## Bond Status Calculation

Each TDLR license record includes an `expire_date` field representing the expiration date of the licensee's required surety bond.

Status is calculated as:
- **Active:** `expire_date` > today
- **Expiring:** `expire_date` is within 30 days of today
- **Expired:** `expire_date` <= today

For this compliance report, "expired" includes both "expired" and "expiring" statuses, as both represent inadequate consumer protection.

## Compliance Rate

For each license type:
```
expired_pct = (count where expire_date <= today) / (total count) * 100
```

## Grading Scale

Grades are assigned based on expired bond percentage:
- **A** — < 10% expired
- **B-** — 10–19% expired  
- **C** — 20–29% expired
- **D** — 30–39% expired
- **F** — >= 40% expired

## Limitations

1. The TDLR dataset reflects information as submitted to TDLR. Some records may have data entry errors.
2. Bond expiration dates in TDLR records reflect the most recently submitted bond, not necessarily all coverage gaps.
3. Some license types (e.g., cosmetology) may not require surety bonds — these were excluded from the compliance analysis.
4. Data is updated monthly; the compliance snapshot reflects conditions at the time of data download.

## Verification

The full dataset is available at [data.texas.gov](https://data.texas.gov/dataset/TDLR-Licensees/7358-krk7). Results can be reproduced by downloading the dataset and computing `expire_date <= CURDATE()` by license type.

Live lookups for individual licensees: [verify.quantumsurety.bond](https://verify.quantumsurety.bond)
