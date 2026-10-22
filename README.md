# DetentionDesk

[![GitHub stars](https://img.shields.io/github/stars/aamirtechs/detentiondesk?style=social)](https://github.com/aamirtechs/detentiondesk/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/aamirtechs/detentiondesk?style=social)](https://github.com/aamirtechs/detentiondesk/network/members)
[![GitHub issues](https://img.shields.io/github/issues/aamirtechs/detentiondesk)](https://github.com/aamirtechs/detentiondesk/issues)
[![License: MIT](https://img.shields.io/badge/License-MIT-gold.svg)](LICENSE)

**A dispatcher-side accessorial recovery ledger for 2 to 20 truck fleets with no TMS.**

DetentionDesk tracks every detention, TONU, layover and lumper fee across every truck, from owed to paid, and builds a printable claim packet in one click. It is a single self-contained HTML file. No build step, no server, no account, no paid APIs. All data stays in the browser on your own device.

## The problem

Small fleets and their dispatchers lose thousands of dollars a year because accessorial fees their drivers earned are never billed or never followed up.

- ATRI puts the cost of detention at $3.6B in direct expenses plus $11.5B in lost productivity in 2023.
- Facilities pay fewer than half of the detention invoices submitted.
- Detention occurs on 39.3% of stops.

The money does not usually die at the dock. It dies in the paperwork: waits scribbled on paper, free time terms buried in old rate cons, claims that sit unsent, and denied claims nobody follows up. Existing tools are either single-driver timers or full TMS platforms you have to migrate to. DetentionDesk is the lightweight middle: a claim pipeline for fleets that still run on spreadsheets and texts.

## Features

- **Accessorial log per load.** Type (detention, TONU, layover, lumper, extra stop, other), load ref, broker, facility, truck, driver, date, arrival and departure times, free time hours, hourly rate or flat fee, notes, and a separate evidence notes field.
- **Broker templates.** Save each broker's default free time and rate once, then apply it in one click. A matching template is applied automatically when a timer is stopped.
- **Live in and out timer.** Start a timer per truck at check in, run several trucks at once, and stop at checkout to stamp arrival and departure into a pre-filled detention entry. Timers survive a page reload.
- **Auto math.** Owed amount is computed automatically: billable hours beyond free time times the hourly rate, or the flat fee in flat mode. Worked check: 3.5 hours waited, 2 hours free, $75 per hour equals $112.50 owed.
- **Unbilled to Paid pipeline.** Every fee sits in Unbilled, Claimed, Denied or Paid. Anything Unbilled for over 48 hours is flagged red, and every Denied entry is flagged red, so slipping money is impossible to miss.
- **Printable claim packet.** One click prints a clean packet with carrier details, broker, load ref, rate con terms, in and out timestamps, the elapsed and billable math, the amount owed, and notes plus evidence notes. Each packet carries the footer: Packet built with DetentionDesk.
- **Recovery dashboard.** This month's claimed, paid and leaked dollars, recovered rate percent, worst facilities ranked by dollars owed, and slowest brokers ranked by outstanding dollars.
- **CSV export.** One click export of all entries, including the full math columns, for your records or your factoring company.
- **Detention Leak Calculator.** Enter loads per week, average wait beyond free time, your rate per hour, and the percent you actually bill, and see your leaked dollars per year and per month.

## How to run

1. Download or clone this repository.
2. Open `index.html` in any modern browser.

That is it. There is no build step, no server, and nothing to install. The only external request is Google Fonts (Sora, Plus Jakarta Sans, IBM Plex Mono), and the tool still works with system font fallbacks if fonts cannot load.

Data lives in `localStorage` in the browser on the device where you use the tool. Clearing browser site data deletes the ledger, so export a CSV regularly and keep it with your load records as your backup.

## Demo data

The app starts empty. To see everything working in under a minute:

1. Open `index.html`.
2. Click **Load demo data** in the top bar. This adds 4 sample entries (one claimed, one unbilled and flagged, one paid, one denied) so the dashboard, rankings and claim packet light up instantly.
3. Open any entry and print its claim packet.
4. Click **Clear all data** when you are ready to start with your own loads.

## Pricing vision

DetentionDesk is free to use in this repository form. The planned hosted tiers, for context on where the product is headed:

- **Free tier:** 1 truck, 5 claim packets per month.
- **Solo dispatcher, $19/mo:** up to 5 trucks.
- **Fleet, $39/mo:** up to 15 trucks.

For scale: a single recovered TONU claim (typically $150 to $400) or two hours of detention at standard rates pays for a year of the solo tier.

## Roadmap

- **v2: photo evidence.** Attach signed BOL photos, lumper receipts and ELD screenshots to an entry and include them in the claim packet. In v1, list what proof you hold in the evidence notes field and keep the files with the load paperwork.
- **v2: denied claim follow-ups.** A follow-up sequence and reminders for denied claims, so a denial is the start of a conversation, not the end of the money.
- Later candidates: CSV or TMS import, and a facility detention scoreboard built from your own history.

## License

MIT License. See [LICENSE](LICENSE) for the full text.

Copyright 2026 Amir Hussain / Dispatch Authority.

---

Built by Dispatch Authority. Packet built with DetentionDesk.
