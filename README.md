# BELOW ZERO — Student Hackathon

This repository contains the built static site for the **BELOW ZERO** student hackathon.

## Run locally

Because the app loads JavaScript as an ES module, serve the repository over HTTP instead of opening `index.html` directly from the file system.

```bash
# From the repository directory
python3 -m http.server 4173
```

Then open <http://localhost:4173> in your browser.

Alternatively, any static file server can be used (for example, VS Code Live Server).

## Fixed blank-screen issue

The HTML entry point now references the JavaScript and CSS bundles from their actual root-level locations. Previously it requested them from a non-existent `assets/` directory, so the React app never mounted and the browser displayed a white screen.
