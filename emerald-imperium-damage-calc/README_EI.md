# Emerald Imperium Damage Calculator (1.3) — patched fork

Fork of harryjowright/emerald-imperium-damage-calc with:

- `src/js/data/sets/normal.js` regenerated: 139 boss battles (★) from Flash Ketchum's battle docs
  + every other trainer from the EI 1.3 game data (1,532 sets total).
  Sets tagged `[HL]`, `[HL-1]`, ... scale with the player's highest level (`levelOffset` field).
- "Your highest Lv" input in the header (`index.template.html`, `js/shared_controls.js`).
- Data patches in `calc/src/data`: Palkia-Primal, custom mega stones (Luxrite, Infernapite,
  Slakite, Empoleonite D/O, Roseradite, Torterrite, Dusknoirite, Grimmite, Applite),
  Kicking Shoes (1.1x kick moves, `calc/src/mechanics/gen789.ts`), ability "THE GRIPPER".
- Top nav bar removed; unused gen 1-8 set files emptied.

## Deploy on GitHub Pages
1. Push this repo to GitHub (branch `master`).
2. Settings → Pages → Source: **GitHub Actions**. The included `.github/workflows/deploy.yml`
   runs `npm install && node build` and publishes `dist/`.

## Build locally
    npm install && (cd calc && npm install)
    node build            # output in dist/index.html
