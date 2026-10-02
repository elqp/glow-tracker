# Glow Tracker

Live mobile app: https://elqp.github.io/glow-tracker/

Glow Tracker is an installable, mobile-first treatment journal for OneDoc JB facial packages under Elaine, Fiona, Sarah and Beulah. The site has spa-inspired visuals, package and dated visit notes, remaining-session balances, and optional MYR/SGD package prices. The saved original price stays in its entered currency; the other amount is an indicative conversion using a dated daily reference rate from [Frankfurter](https://frankfurter.dev/), not a clinic or card payment quote. The frontend is hosted from this repository's `main` branch on GitHub Pages; the separately published Glow Tracker API stores packages and visits in a shared managed database across devices.

**Name-only profiles are not authentication.** Anyone who can open the site or API can select, view, change or delete any of the four profiles' records. Please do not enter sensitive medical information. This is an independent journal, not OneDoc JB's official records. Shared records and currency conversion require internet access, although the installable app shell is cached after first use.

The previous Google Sheets version remains in this repository's Git history at commit `f9cd084`. Its external Sheet, if any, was not deleted or migrated. The new shared database starts empty. A `gh-pages` branch holds the initial static deployment as a rollback reference; it is not the active Pages source.

The compiled site files, including two self-hosted spa WebP images, are in this repository root. Source code and the backend are maintained in the Manus Glow Tracker project. Build that source with `VITE_API_BASE_URL=https://glowtracker.manus.space/api pnpm build`, then commit the `dist/` contents here to update Pages.
