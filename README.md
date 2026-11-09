# AI Football Prediction Agent — Android PWA

Free browser-based progressive web app. No Termux, APK sideloading, Windows PC, paid cloud, or server-side database. Match data and paper bets are stored in IndexedDB in the Chrome profile on the tablet.

## Publish for free with GitHub Pages
1. Create a public repository on GitHub.
2. Upload all files in this folder to the repository root.
3. Open repository Settings → Pages.
4. Select deploy from branch `main`, folder `/ (root)`, and save.
5. Wait for the HTTPS Pages address, then open it in Chrome on Android.
6. Chrome menu ⋮ → Install app / Add to Home screen.

PWA installation and service-worker offline caching require HTTPS or localhost. GitHub Pages is used only to serve static files; user records remain in the tablet's browser storage.

## Use
- Matches: enter league shortcut (Bundesliga commonly `bl1`) and season year; import from OpenLigaDB.
- Predict: select teams. At least 12 completed matches are needed.
- Backtest: at least 25 completed matches are needed.
- Paper bets: record virtual bets manually; no real bets are placed.
- Export matches to CSV regularly.

## Limits
OpenLigaDB coverage varies and it does not supply a complete archive of historical bookmaker odds. Therefore the app does not claim valid historical ROI or closing-line value. The Poisson model is an experimental baseline, not a proven profitable AI. A 20% daily return cannot be guaranteed. This first PWA MVP does not yet include bet settlement, Elo-based blended probabilities, automatic daily scheduling, or a full JSON restore/backup workflow.

If the import fails, check the league/season and internet connection. If OpenLigaDB blocks browser requests on a particular network/browser, an import proxy would be needed; that would introduce a hosted service and is intentionally not included in this fully local/static build.
