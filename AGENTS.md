# AGENTS.md

## Cursor Cloud specific instructions

This is a Next.js 14 client-side-only web app (Secret Emoji Encoder). There are no backend services, databases, or external API dependencies.

### Key commands

- **Install deps:** `npm install --legacy-peer-deps` (required due to `date-fns@4` vs `react-day-picker@8` peer conflict)
- **Dev server:** `npm run dev` (serves at `http://localhost:3000`)
- **Lint:** `npm run lint`
- **Build:** `npm run build`

### Gotchas

- The original `package.json` does not include ESLint or `eslint-config-next` as devDependencies. These are added in the dev setup branch (`.eslintrc.json` + devDeps). Without them, `npm run lint` will prompt interactively.
- ESLint must be v8 (not v9) and `eslint-config-next` must match the Next.js version (`14.2.16`) to avoid config errors.
- `npm install` without `--legacy-peer-deps` fails due to a peer dependency conflict between `date-fns@4.1.0` and `react-day-picker@8.10.1`.
