# Changelog

All notable changes to DetentionDesk are documented in this file.

## v1.0.0, 2026-10-22

First release.

- Accessorial log per load for detention, TONU, layover, lumper, extra stop and other fees, with broker, facility, truck, driver, date, in and out times, free time, hourly rate or flat fee, notes and evidence notes.
- Broker templates that save a broker's default free time and rate and apply in one click, including automatic application when a timer is stopped.
- Live in and out timer per truck, with multiple timers running at once, surviving page reloads, stamping arrival and departure into a pre-filled detention entry.
- Auto math: billable hours beyond free time times the hourly rate, or the flat fee in flat mode, with a live preview while entering a fee.
- Claim pipeline from Unbilled to Claimed to Denied to Paid, with red flags for entries Unbilled over 48 hours and for all Denied entries.
- One click printable claim packet with carrier details, rate con terms, timestamps, elapsed and billable math, amount owed, and the DetentionDesk footer.
- Recovery dashboard with claimed, paid and leaked dollars this month, recovered rate percent, worst facilities and slowest brokers ranked.
- CSV export of all entries including the full math columns.
- Detention Leak Calculator showing leaked dollars per year and per month.
- Demo data button with 4 sample entries, and a clear all data option. The app seeds empty by default.
- Local-first design: a single self-contained HTML file, all data in browser localStorage, no server, no account, no paid APIs.
