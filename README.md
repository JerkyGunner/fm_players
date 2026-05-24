# FM Players

`fm_players` is a browser-based tool for scoring Football Manager player exports against role attribute weightings.

## How it works

The app ships with a built-in set of role weightings stored in `assets/data/roles.json`.

When you use the app:

1. Select one or more roles to score against.
2. Upload an exported Football Manager HTML file.
3. The app reads the table in your browser.
4. Each player is scored against the selected role weightings.
5. The results table shows role scores, the best-matching role, and a few utility metrics.

All processing happens in the browser. The app does not need a backend server or database.

## Expected input

The uploaded file should be:

- An HTML export from Football Manager
- In English
- Exported with all required attributes visible

If expected columns are missing, score calculation will fail and the app will show an error.

## Included FM views

The repository includes Football Manager view files in `FMviews/`:

- `all_attributes_shortlist.fmf`
- `all_attributes_squad.fmf`
- `player search all attributes.fmf`

These can be imported into Football Manager to help produce compatible HTML exports with the attributes this app expects.

## Role weightings

The default role weightings are loaded from `assets/data/roles.json` and then cached in browser storage.

You can:

- Select which roles to include in scoring
- Edit role weightings in the app
- Restore the default weightings from the bundled JSON file

## Running locally

Because this is a static web app, you can run it with any simple local web server.

One easy option is:

1. Open the project folder in Visual Studio Code.
2. Start a local server such as the Live Server extension.
3. Open `index.html` through that local server.

## Hosting

This project can be hosted as a static site on services such as GitHub Pages or Cloudflare Pages.
