# Word Explorer

A customizable classroom word game, published at [scottsummers.github.io/word-explorer](https://scottsummers.github.io/word-explorer/).

The game is fully self-contained: it loads no scripts, fonts, or other assets from outside this repository, so it works on a locked-down school network.

## Layout

- `index.html` — page shell, self-hosted `@font-face` rules, and script tags
- `favicon.svg` — local tab icon
- `src/app.jsx` — the game source (React/JSX). Edit this file.
- `app.js` — compiled output, served by GitHub Pages. Commit this whenever you change the source.
- `vendor/` — React 18.3.1 and ReactDOM production UMD builds (MIT license)
- `fonts/` — Nunito and Fredoka (SIL Open Font License 1.1)

## Building

After changing `src/app.jsx`, rebuild `app.js` and commit both files:

```bash
npx --yes esbuild src/app.jsx --outfile=app.js --jsx=transform --target=es2018
```

No other build step is needed. Open `index.html` over a local static server (for example `python3 -m http.server`) to try it.

## License notes

React and ReactDOM are MIT-licensed; copies of the licenses are in `vendor/`. Nunito and Fredoka are licensed under the SIL Open Font License 1.1; copies are in `fonts/`.
