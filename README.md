# Glow Tracker

Live mobile app: https://elqp.github.io/glow-tracker/

Glow Tracker is an installable treatment journal for One Doc JB Southkey facial packages under Elaine, Fiona, Sarah and Beulah. Each visit can use one or more sessions, and package cards show the resulting balance. Profiles can record package and visit notes, optional MYR/SGD package prices with dated reference conversions from [Frankfurter](https://frankfurter.dev/), and a shared next appointment date editable on the name-selection page. The Packages tab offers a JSON export of the selected profile's records.

The ONEDOC tab links to the [Southkey WhatsApp business account](https://wa.me/60183885168) at **+60 18 388 5168**, matching [One Doc's official outlet listing](https://www.onedoc.com.my/our-outlets/). The displayed hours were supplied for this app: **Monday–Saturday 10 am–7 pm; Sunday 10 am–5 pm**. The link opens WhatsApp but sends no message or treatment data automatically.

**Name-only profiles are not authentication.** Anyone who can open the site or API can select, view, change or delete any profile's records. Please do not enter sensitive medical information. This is an independent journal, not One Doc's official records. Shared records, appointments and currency conversion need internet access, although the installable app shell is cached after first use.

The previous Google Sheets version remains in Git history at commit `f9cd084`; any external Sheet was not deleted or migrated. Existing data in the new shared database is retained across app updates. A `gh-pages` branch holds the initial static deployment as a rollback reference; GitHub Pages currently serves this repository's `main` branch.

The compiled site, including self-hosted spa WebP images, is in this repository root. Source code and the backend are maintained in the Manus Glow Tracker project. Build that source with `VITE_API_BASE_URL=https://glowtracker.manus.space/api pnpm build`, then commit the contents of `dist/` here to update Pages.
