# Awesome-Multi-Currency-Autonomous-Bookkeeping

# Awesome-Multi-Currency-Autonomous-Bookkeeping

## Top Multi-Currency Autonomous Bookkeeping Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Multi-Currency Reconciliation, AI-Powered Transaction Matching & Autonomous Financial Close*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Multi-Currency Autonomous Bookkeeping**. These tools use AI to match bank ledger entries with operational receipts, invoices, and payment records across currencies — automating reconciliation, categorization, and month-end close without manual data entry.

**Examples** include Numeric, Rillet, Digits, Vic.ai, Puzzle, Truewind, Docyt, Booke AI, Campfire, and Osfin AI (the category leaders).

**Open-source emphasis**: This section is expanded with every major active project for self-hosting, custom reconciliation engines, and transparent multi-currency accounting — ideal for finance teams prioritizing data sovereignty, developers building bookkeeping pipelines, and organizations avoiding per-transaction SaaS pricing.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Numeric](https://www.numeric.io/)**  
  AI-powered accounting close platform that centralizes the entire close process, monitors financial data, detects anomalies, and tracks task completion. Best for accounting teams and controllers managing complex monthly and quarterly closes. Custom enterprise pricing, no free plan .

- **[Rillet](https://www.rillet.com/)**  
  Revenue recognition and financial close automation built specifically for SaaS companies. Connects directly to Stripe and billing systems to continuously update revenue schedules aligned with ASC 606 and IFRS 15. Custom pricing .

- **[Digits](https://digits.com/)**  
  AI financial insights for small businesses with automated transaction analysis, real-time dashboards, and plain-English explanations of business performance. Offers a free plan for basic usage, with paid tiers for advanced reporting .

- **[Vic.ai](https://www.vic.ai/)**  
  AI-driven invoice processing and predictive GL coding for enterprise AP teams. Features duplicate invoice detection, automated approval workflows, and real-time AP analytics. Custom enterprise pricing based on invoice volume .

- **[Puzzle](https://puzzle.io/)**  
  AI-native accounting software designed for startups and accounting firms. Real-time reconciliation, automated month-end close, and daily financial insights. **No public free plan** .

- **[Truewind](https://www.truewind.ai/)**  
  Combines AI-powered bookkeeping with professional accountant review for venture-backed startups. Automates transaction categorization, reconciliations, and month-end close with human oversight. Custom pricing .

- **[Docyt](https://docyt.com/)**  
  AI-powered bookkeeping automation for multi-location businesses and franchises, with document collection and reconciliation.

- **[Booke AI](https://www.booke.ai/)**  
  AI-powered bookkeeping automation for QuickBooks and Xero. Uses AI and RPA to reduce manual work by 80% through automated reconciliation, smart document processing, and proactive error detection. Paid plans from $20 .

- **[Campfire](https://campfire.ai/)**  
  AI-powered accounting platform with autonomous bookkeeping and real-time financial close for startups.

- **[Osfin AI](https://www.osfin.ai/)**  
  Financial operations platform automating transaction categorization, bank reconciliation, AP/AR management, and financial close. Handles high-volume transaction environments with real-time dashboards. Targets growth-stage and established companies .

## Open-Source GitHub Projects

- **[MA3 Reconciliation Engine](https://www.npmjs.com/package/@idriszade/ma3-reconciliation-engine)**  
  **Cross-source record matching for any structured data** — bank vs ledger, PO vs receipt vs invoice, billing vs accounting. Returns matched records, discrepancies, and unmatched items with LLM-generated explanations. **Matching is 100% pure computation with no LLM involvement** — the LLM fires only when exceptions exist. Supports exact or fuzzy matching with amount and date tolerances. Includes multi-currency wire matching by key and batch payment splitting scenarios. 19+ tests covering payroll GL discrepancies, timezone tolerance, and month-end 50-transaction perfect close .

- **[reconcile-py](https://pypi.org/project/reconcile-py/0.1.0/)**  
  **Deterministic Python library for bank-to-ledger reconciliation.** Pure and deterministic — no wall-clock time, no randomness. Shuffling input order produces byte-identical results. Features `FieldRule` for gate and graded matching criteria (amount gates with absolute or percentage tolerance, date gates with day windows, reference and counterparty similarity grading). Returns matches with `Reason` objects (which gates passed, each graded similarity) for full explainability. Pandas adapter handles dtype quirks including NaN/NaT normalization and exact decimal conversion .

- **[Reckon](https://github.com/cantino/reckon)**  
  **Flexibly import bank account CSV files into Ledger** for command-line accounting. Uses **Bayesian machine learning** to select the correct accounts associated with CSV data. Supports unattended mode with `--learn-from` an existing ledger file or `--account-tokens` YAML for keyword-based account assignment. Handles multiple currencies via `-c` currency symbol flag. Ruby gem, installable via `gem install reckon` .

- **[Firefly III](https://github.com/firefly-iii/firefly-iii)**  
  **Self-hosted personal finance manager with powerful rule engine.** Rule triggers include transaction type, reconciliation status, attachments, categories, budgets, tags, amount (with foreign amount and currency filters), source/destination account (ID, name, IBAN, number), and date/time. All triggers can be inverted with the "NOT" option. Amount triggers handle bigger than, less than, exactly. Foreign currency triggers available for multi-currency transactions . AGPL-3.0 licensed.

- **[GnuCash](https://github.com/Gnucash/gnucash)**  
  **Free, open-source double-entry accounting for personal and small business use.** Full **multiple currency support** — track bank accounts, investments, and financial data in different currencies with real-time exchange rates . Statement reconciliation via QIF import and "druid" wizard. Production-stable since 1999, available for Linux, Windows, and macOS. GPL licensed .

- **[ERPNext](https://github.com/frappe/erpnext)**  
  **Full open-source ERP with bookkeeping and multi-currency out of the box.** Bank reconciliation to clear bank data entry discrepancies. Handles multiple currencies natively — no ad-hoc conversions needed . Python/Frappe framework, GPL-3.0 licensed.

- **[LedgerSMB](https://github.com/ledgersmb/LedgerSMB)**  
  **Free double-entry accounting and ERP system** for small and medium businesses. Production-stable since 2006. PostgreSQL backend with multilingual support . GPL-2.0 licensed.

- **[Beancount + Fava](https://github.com/beancount/beancount)**  
  **Plain-text double-entry accounting with powerful visualization.** Beancount processes plain-text ledger files; Fava provides web-based dashboards with treemaps, net worth tracking, and monthly comparison charts . Supports multi-currency ledgers with automatic balance assertions. Can be automated via cron jobs fetching bank APIs and appending transactions — enabling near-real-time financial visibility while maintaining full control and transparency .

- **[Transity](https://github.com/ad-si/Transity)**  
  **Plain text accounting with YAML journal files and AI-powered import.** Built-in OpenAI GPT converts any financial data (CSVs, bank statements, chat history) to Transity journal format . Ledger CLI import script included. Focus on physical accounts and tags rather than abstract ledger accounts.

### Additional Strong Open-Source Options

- **Bizuno Accounting** — Full ERP/accounting/CRM for WordPress. Trusted evolution of PhreeBooks since 2007. Self-hosted, no subscriptions. Multi-warehouse and multi-business support from one instance. US tax calc via API, shipping integrations with USPS, FedEx, UPS .
- **FrontAccounting** — Web-based open-source accounting solution with basic ERP functionality. GPL licensed .
- **TurboCASH** — Open-source accounting management program. GPL licensed .
- **HomeBank** — Personal accounting management software. GPL licensed .

**Frameworks for building custom systems**: Combine **MA3** for cross-source matching with pure computation and LLM exception handling, **reconcile-py** for deterministic bank-to-ledger reconciliation with full explainability, **Reckon** for Bayesian account assignment from bank CSVs, **Beancount + Fava** for plain-text multi-currency ledgers with real-time dashboards, and **Firefly III** or **GnuCash** for self-hosted double-entry accounting to build a complete open-source multi-currency bookkeeping stack.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Multi-currency bookkeeping tools must comply with local accounting standards (GAAP, IFRS), tax regulations, and data protection laws. **AI-categorized transactions and automated reconciliations must be reviewed by qualified accountants before finalizing books** — errors in multi-currency conversions, FX gain/loss treatment, and intercompany eliminations can have material financial reporting consequences.
- Self-hosted open-source solutions require proper security hardening, backup strategies, and accounting domain expertise for configuration.

---

**Made for controllers, finance teams, accounting firms, and developers building autonomous bookkeeping platforms.**  
Let's make multi-currency autonomous bookkeeping more open, accurate, and finance-team friendly.
