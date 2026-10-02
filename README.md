# Glow Tracker

Live mobile app: https://elqp.github.io/glow-tracker/

Glow Tracker is a personal treatment journal for OneDoc JB facial packages under Elaine, Fiona, Sarah and Beulah. The mobile-first static frontend is published from this repository's `main` branch on GitHub Pages. It connects to the separately published [shared API](https://onedocjb-4hgxba3z.manus.space/_app/health), which stores packages and treatment sessions in a managed database across devices.

**Name-only profiles are not authentication.** Anyone who can open the site or API can select, view, change or delete any of the four profiles' records. Please do not enter sensitive medical information. This is an independent journal, not OneDoc JB's official records.

The previous Google Sheets version remains in this repository's Git history at commit `f9cd084`. Its external Sheet, if any, was not deleted or migrated. The new shared database starts empty.

The compiled site files are in the repository root. The source application and backend are maintained in the Manus Glow Tracker project; updating this Pages site requires building that source with `VITE_API_BASE_URL=https://onedocjb-4hgxba3z.manus.space/api` and committing the resulting `dist/` files here. A `gh-pages` branch also contains the same initial deployment as a rollback reference.
