# Redis Real-Time Decisioning Demos

Interactive walkthroughs of the Redis Real-Time Decisioning architecture, built for specific enterprise accounts.

## Structure

```
/
├── index.html          Landing page with links to all demos
├── vercel.json         Vercel routing config
├── ulta/
│   └── index.html      Ulta Beauty demo
└── vizio/
    └── index.html      Vizio demo
```

## Adding a new demo

1. Create a new folder at the root (e.g. `/tmobile/`)
2. Drop the demo HTML file inside as `index.html`
3. Add a card to the landing page `index.html`
4. Commit and push — Vercel auto-deploys

## URLs (after deploy)

- `/` — Landing page
- `/ulta` — Ulta Beauty demo
- `/vizio` — Vizio demo

## Local preview

Just open `index.html` in a browser, or run a quick local server:

```
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.
