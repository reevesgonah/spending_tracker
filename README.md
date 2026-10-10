# Spending Tracker

A simple, mobile-first web app for logging everyday spending against budgets, built for quick entry on a phone without opening a spreadsheet.

**Live app:** https://reeves-spending-tracker.netlify.app

## Features

- **Quick logging**: pick a category, enter an amount, optional note, done.
- **Budgets per category**: starts with Transport, Lunch and Airtime; edit budgets or add and delete your own categories.
- **Live progress bars**: see spent vs budget for each category, turning red when you go over.
- **Pay-cycle tracking**: your "month" starts when you say so, not on the 1st. Tap **New pay cycle starts today** on payday and the totals reset, while all past entries stay in History.
- **History**: every entry in one list, with delete.
- **Export**: download a CSV, or **Copy CSV** to paste into Sheets/Excel (useful in in-app browsers that block downloads).
- Light and dark mode follow your device setting.

## Privacy

There is no server, no account and no tracking. Everything you enter is stored in your own browser's `localStorage`, so each person who opens the app starts with an empty tracker and only ever sees their own data.

Because data lives in the browser:

- Clearing site data or switching browser/phone wipes it. Export or copy your CSV regularly as a backup.
- It does not sync between devices.

## Run locally

It is a single static file with no build step.

```
git clone <this-repo-url>
cd spending-tracker
# open index.html in a browser
```

## Deploy your own copy

- **Netlify**: drag the folder (or just `index.html`) onto https://app.netlify.com/drop
- **GitHub Pages**: Settings > Pages > deploy from the `main` branch root.

## Customising

Default categories and budgets are defined at the top of the script in `index.html` (the `state` object). Currency is shown as KES; change the `fmt` function to use another.

## Known limitations

- Single user, single device per browser.
- File download may not work inside some wrapper/in-app browsers; use **Copy CSV** there.

## License

MIT, see [LICENSE](LICENSE).
