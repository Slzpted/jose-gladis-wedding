# Jose & Gladis — Wedding Invitation

A single-page animated wedding invitation site (envelope opening intro, countdown timer, event details, and an RSVP form) for **08.29.2026**.

## Live Demo

Once deployed to GitHub Pages, this will be available at:

```
https://<your-username>.github.io/<repo-name>/
```

## Features

- Animated "open the envelope" landing intro
- Countdown timer to the wedding date
- Event details with tap-to-open Apple Maps / Google Maps links
- RSVP form (submits to [Formspree](https://formspree.io/))
- Fully self-contained — no build step, no dependencies to install

## Getting Started

This is a static, single-file site — no build tools required.

1. Clone the repo:
   ```bash
   git clone https://github.com/<your-username>/<repo-name>.git
   cd <repo-name>
   ```
2. Open `index.html` directly in a browser, or serve it locally:
   ```bash
   python3 -m http.server 8000
   ```
   then visit `http://localhost:8000`.

## Deploying with GitHub Pages

1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to `Deploy from a branch`.
4. Choose the `main` branch and `/ (root)` folder, then save.
5. Your site will be published at `https://<your-username>.github.io/<repo-name>/`.

## Configuration

Before deploying for your own event, update the following in `index.html`:

- **Names, dates, and copy** — search for "Jose & Gladis" and the event date (`2026-08-29`) and replace with your own.
- **Countdown target** — the `startCountdown()` function targets `2026-08-29T16:00:00`; update to your event's date/time.
- **Venue coordinates** — the `openMap()` calls use hardcoded latitude/longitude pairs; replace with your venues' coordinates.
- **RSVP form endpoint** — the form currently posts to a Formspree endpoint (`https://formspree.io/f/mgobdjvn`). [Create your own Formspree form](https://formspree.io/) and swap in your own endpoint ID so RSVP submissions go to you, not the original couple.

## Tech Stack

- Plain HTML, CSS, and vanilla JavaScript (no framework, no build step)
- Google Fonts: Cormorant Garamond, Pinyon Script, Jost
- [Formspree](https://formspree.io/) for RSVP form handling

## License

This project is provided as-is for personal, non-commercial use. Feel free to fork and adapt it for your own event.
