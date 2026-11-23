# Open CapIQ Workbench

A one-page web app for open-source equity research and MBA valuation. It does two things:

1. **Maps the open-source alternatives to S&P Capital IQ** (OpenBB, SEC EDGAR, FinanceToolkit, FinanceDatabase, yfinance). For each tool it lists what you get, the licence and what to watch out for, and it lists what you give up by leaving a paid terminal.
2. **Runs the core MBA valuation methods live in the browser.** Change any assumption and the result updates as you type.

**Live:** https://komalkedarnath.wiki/open-capiq-workbench/

There are no dependencies and no build step. The whole app is one HTML file.

## What is inside

Every tab has its own link, so you can send someone straight to a method.

| Tab | What it does | Link |
| --- | --- | --- |
| Open-source stack | The five tools, their licences and limits, and what you give up against Capital IQ. | [`#landscape`](https://komalkedarnath.wiki/open-capiq-workbench/#landscape) |
| DCF | Five years of free cash flow plus a terminal value. Gives enterprise value, equity value, value per share and the share of value that sits in the terminal. A sensitivity table runs WACC against terminal growth in half-point steps. | [`#dcf`](https://komalkedarnath.wiki/open-capiq-workbench/#dcf) |
| WACC | CAPM cost of equity (risk-free rate plus beta times equity risk premium), after-tax cost of debt, and the weighted result. One click sends the WACC to the DCF. | [`#wacc`](https://komalkedarnath.wiki/open-capiq-workbench/#wacc) |
| DuPont | Return on equity split into net margin, asset turnover and financial leverage, to show where the return comes from. | [`#dupont`](https://komalkedarnath.wiki/open-capiq-workbench/#dupont) |
| Comps | Peer median EV/EBITDA and P/E applied to a target company, giving implied enterprise value and equity value. | [`#comps`](https://komalkedarnath.wiki/open-capiq-workbench/#comps) |
| NPV / IRR | A run of cash flows from year 0 against a discount rate. Gives NPV, IRR (found by bisection), payback with interpolation, and the accept or reject rule. | [`#npv`](https://komalkedarnath.wiki/open-capiq-workbench/#npv) |

## The open-source stack

| Tool | What it gives you | Licence |
| --- | --- | --- |
| OpenBB Platform | One Python interface over many data providers, plus a terminal and workspace. | AGPL-3.0 |
| SEC EDGAR | Filings, XBRL financial facts, insider and ownership forms for US-listed companies. | Public data |
| FinanceToolkit | 150+ ratios and models (DuPont, WACC, DCF) computed from statements, with transparent formulas. | MIT |
| FinanceDatabase | A searchable universe of equities, ETFs and funds by sector, industry and country, for building peer sets. | MIT |
| yfinance | Prices, basic fundamentals and estimates pulled from Yahoo Finance. | Apache-2.0 |

## What you give up

Open data is good enough for learning, screening, public-company valuation and first drafts. Pay for a terminal when you need clean estimates, private-market data or an audit trail your clients will accept.

| Capability | Capital IQ | Open stack |
| --- | --- | --- |
| Standardised, restated, point-in-time financials | Yes | DIY |
| Broker consensus estimates | Yes | Thin |
| Private company, M&A and funding data | Yes | Very limited |
| Global coverage and ownership | Yes | US-strong |
| Cost, auditability, scriptability | Per-seat licence | Free and transparent |

## Run it

Use the live page above, or open `index.html` in a browser. Nothing needs installing.

## Limits

- Educational use only, not investment advice. Every input is your own assumption.
- The peer data in the Comps tab is fictional placeholder data. Pull a real peer set with FinanceDatabase and OpenBB.

Part of the projects and research listed at https://komalkedarnath.wiki/research/.
