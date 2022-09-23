# VPS Rollup External Bug

## Prior Setup

1. Added `<img src="/test">` to `index.page.vue`.
2. Added `build: { rollupOptions: { external: ["/test"] } }` to `vite.config.js`.

## Reproduction

1. Run `npm install`.
2. Run `npm run build` or `npx vite build`.
3. See error in terminal.
4. Go to `dist/server/assets/index.page.<hash>.js`.
5. See `import _imports_0 from "../../../../../../../../../test";`.
