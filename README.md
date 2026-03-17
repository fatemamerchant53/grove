# Grove

A relationship pipeline built for legal professionals. Grove helps lawyers track their professional network across in-house, firm, and government contacts — with health scores, AI-powered weekly outreach plans, and a gathering generator to put the right people in the same room.

Open source, single file, no account required. Your data stays on your device.

---

## What it does

- **Relationship health scores** — every contact gets a 0–100 score based on how recently you've been in touch, calibrated to their pipeline stage
- **Pipeline stages** — move contacts through New → Warm → Active → Outcome
- **Contact type tracking** — in-house, law firm, government, or other
- **Location filtering** — heading to Houston for a conference? Filter your contacts by city and sort by relationship depth
- **Weekly outreach plan** — AI-generated mix of texts, coffees, lunches, and emails for the week
- **Gathering generator** — describe an occasion and the AI suggests who to put in the room together, and why
- **Touchpoint logging** — one-click to log a coffee, call, or email without opening the full edit form
- **Export / Import** — download your data as a JSON backup file and restore it any time
- **No account, no server, no tracking** — everything lives in your browser

---

## Getting started

### Option 1 — Open directly in your browser

Download `grove.html` and open it in any modern browser. That's it.

### Option 2 — Use the hosted version

Visit `https://fatemamerchant53.github.io/grove` — no download required.

### Option 3 — Serve locally
```bash
python -m http.server 8000
```

Then open `http://localhost:8000/grove.html`.

---

## Importing your contacts

### From LinkedIn

1. Go to linkedin.com and sign in
2. Click your profile photo → **Settings & Privacy**
3. Go to **Data Privacy → Get a copy of your data**
4. Select **Connections** only → click **Request archive** (arrives ~10 min via email)
5. Download the ZIP and find **Connections.csv** inside
6. In Grove, click **Import CSV** → follow the LinkedIn tab

### From any CSV

Grove recognizes these column names automatically:

| Field | Recognized column names |
|-------|------------------------|
| Name | `name`, `first name`, `last name` |
| Company | `company`, `organization` |
| Role | `title`, `position`, `role` |
| Email | `email`, `email address` |

---

## Backing up your data

Click **Export data** in the top nav to download a `grove-backup-[date].json` file. Save it somewhere safe.

To restore, click **Import data** and select your backup file. Works across browsers and devices.

---

## How health scores work

| Stage | Touch every | Score hits 0 after |
|-------|-------------|-------------------|
| New | 60 days | 60 days |
| Warm | 30 days | 30 days |
| Active | 14 days | 14 days |
| Outcome | 90 days | 90 days |

---

## Tech stack

| | |
|---|---|
| Framework | None — vanilla HTML, CSS, JavaScript |
| Storage | Browser localStorage + JSON export |
| Dependencies | Zero |
| File count | 1 |

---

## License

MIT — use it, fork it, build on it.

*Built with [Claude](https://claude.ai)*
