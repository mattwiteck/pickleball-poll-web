
# Funny Poll (Teams website tab)

This folder contains a tiny static webpage that makes the **“No”** button run away from the mouse, so only **“Yes”** is practically clickable. Perfect for a lighthearted Teams tab prank.

## Files
- `index.html` – The webpage (no build step needed)

## How to use it in Microsoft Teams

### Option A — Fastest: Add as a **Website** tab (no packaging)
1. **Host** the `index.html` somewhere that allows embedding in an iframe, for example:
   - Any simple web host you control
   - Azure Static Web Apps (free tier works great)
   - GitHub Pages (make sure your org allows it)
2. Copy the public **URL** to `index.html`.
3. In the Teams channel where you want the poll, click **+** → **Website** → paste the URL → **Save**.

> Note: Some hosts block embedding via security headers (`X-Frame-Options` or `Content-Security-Policy`). If the page doesn’t show in Teams, host it somewhere that allows embedding in Teams.

### Option B — Package as a custom Teams app (static tab)
If you’d prefer a proper Teams app package, ask your admin to enable **upload custom apps**. I can generate a manifest for you once you have a final URL.

## Optional: Record “Yes” votes
The page includes a commented-out `fetch('/api/vote', ...)` call. If you have an endpoint, you can uncomment it to record votes.

## Accessibility & etiquette
- Provide an alternate way to answer “No” (e.g., reply to the thread), since mouse users get blocked by design.
- Share it in a lighthearted channel and keep the joke brief.
