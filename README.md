# MindCare UI prototype

Interactive design handoff for a responsive web app and a shared Flutter app design for iOS/Android. This repository contains a static HTML prototype, not a Flutter implementation or functioning consultation backend.

## Preview

Hosted preview: https://victor-studios.github.io/mindcare-ui-preview/

- [Web app](https://victor-studios.github.io/mindcare-ui-preview/?surface=web&viewport=desktop)
- [iPhone mockup](https://victor-studios.github.io/mindcare-ui-preview/?surface=app&platform=ios)
- [Android mockup](https://victor-studios.github.io/mindcare-ui-preview/?surface=app&platform=android)

Open `index.html`, or run `python3 -m http.server 8876` from this folder and visit http://localhost:8876.

Select Web app or Mobile app in the preview toolbar. URL variants:
- `?surface=web&viewport=desktop`
- `?surface=web&viewport=mobile`
- `?surface=app&platform=ios`
- `?surface=app&platform=android`

Main navigation: Chat, Screening, Records, Profile. Mobile web and phone app previews use the hamburger menu for these destinations; there is no bottom navigation bar, giving chat more vertical space. Mobile app language and Light/Dark settings are in Profile. Voice-call button uses a handset icon only. Mockup shells approximate iPhone 18 Pro Max and Galaxy S26 Ultra. Brand accents use WhatsApp green (#25D366). Chat uses right-aligned outgoing bubbles (light #D9FDD3, dark #005C4B), left-aligned incoming bubbles (white / #202C33), compact corners and tails. Dark mode retains neutral charcoal surfaces.

## Developer guide

- `index.html`: app shell and SVG icons.
- `style.css`: layout, palette, responsive styling, RTL, themes and device mockups.
- `app.js`: original screens and simulated interactions.
- `bilingual.js`: English/Urdu UI, chat/call sample behavior, independent response language.
- `surfaces.js`: web/app variants, navigation and Profile.
- `theme.js`: appearance preferences.

Load scripts in their existing order. The later files extend the earlier prototype; changes to shared functions must account for these wrappers. No npm dependencies, build command or API keys are required. Assets use relative paths so repository subpath hosting works.

Only language/appearance preferences persist in local storage. Chat messages and profile edits are in memory. AI responses, voice recognition, speech playback, reports and clinical assessment behavior are demonstrations, not integrated services. A developer still needs to implement the production application, backend and Flutter UI.

## GitHub Pages

1. Push these files to the root of the chosen GitHub repository.
2. In Settings → Pages, choose Deploy from a branch.
3. Choose the branch containing these files (usually main), folder / (root), then Save.
4. GitHub provides an HTTPS link of the form https://OWNER.github.io/REPOSITORY/.

GitHub Free Pages supports public repositories. Pages from private repositories requires an eligible paid GitHub plan; repository privacy does not by itself make a Pages site private. Use this as a design demo with sample data.

## Vercel alternative

Import the GitHub repository in Vercel, select the Other framework preset and the repository root. Use no build command and serve this root containing index.html. Vercel supplies a vercel.app URL and supports Git-based deployments. Check plan eligibility: Hobby is limited to personal, non-commercial use, so do not assume an organisational project qualifies merely because it is nonprofit.

## References

- https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages
- https://vercel.com/docs/git
- https://vercel.com/docs/limits/fair-use-guidelines

Updated 27 October 2026.
