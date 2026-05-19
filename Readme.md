# HaulX — Commercial Vehicle Booking

A production-grade commercial vehicle booking webpage. Book passenger buses, goods trucks, container vehicles, and rentals across India.

🌐 **Live site:** `https://<your-github-username>.github.io/haulx-booking`

## Features

- Route search with swap button
- Vehicle type tabs (Passenger, Goods, Container, Rental)
- Live search results with availability badges
- Booking confirmation modal with reference ID
- Fleet showcase with 8 vehicle types
- Fully responsive (mobile + desktop)

## Deploy in 5 minutes

See [DEPLOY.md](DEPLOY.md) for step-by-step instructions.

## Tech Stack

Pure HTML · CSS · Vanilla JS — zero dependencies, zero build step.

## Local Preview

```bash
# Option 1 — just open the file
open index.html

# Option 2 — local server (recommended)
npx serve .
# then visit http://localhost:3000
```

## Project Structure

```
haulx-booking/
├── index.html              ← entire app (self-contained)
├── .github/
│   └── workflows/
│       └── deploy.yml      ← GitHub Actions auto-deploy
├── README.md
└── DEPLOY.md
```

## Customise

| What | Where in index.html |
|---|---|
| Company name / logo | Search `HAULX` |
| Vehicle types & prices | `const vehicles = [...]` |
| Mock search results | `const mockResults = [...]` |
| Colour scheme | `:root { --amber: ... }` |
| Cities / routes | Form placeholders |

## License

MIT