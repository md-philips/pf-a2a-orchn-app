# AGENTS.md

Guidance for AI coding agents working in this repository.

## Project Snapshot

- Stack: React 19 + TypeScript + Vite 8.
- Package manager: npm (lockfile not present yet).
- Baseline docs: [README.md](README.md).

## Fast Start Commands

- Install dependencies: `npm install`
- Start dev server: `npm run dev`
- Build: `npm run build`
- Lint: `npm run lint`
- Preview production build: `npm run preview`

Run `npm run build` and `npm run lint` after non-trivial UI or config changes.

## Code Map

- App bootstrap: [src/main.tsx](src/main.tsx)
- Main UI component: [src/App.tsx](src/App.tsx)
- Global styles: [src/index.css](src/index.css)
- App-specific styles: [src/App.css](src/App.css)
- Vite config (React + compiler preset): [vite.config.ts](vite.config.ts)

## Repository Conventions

- Use TypeScript ESM imports consistent with existing files.
- Keep `App` as a functional React component pattern unless intentionally refactoring.
- Preserve current styling approach (CSS files imported from TSX entry points).
- Prefer incremental edits over broad rewrites in this starter scaffold.

## Tooling Notes

- TypeScript settings include strict cleanliness checks like `noUnusedLocals` and `noUnusedParameters` in [tsconfig.app.json](tsconfig.app.json).
- Vite uses `@vitejs/plugin-react` plus Babel React compiler preset in [vite.config.ts](vite.config.ts); keep both unless there is an explicit migration decision.
- ESLint config is flat-config based in [eslint.config.js](eslint.config.js).

## Known Gaps

- No test framework is configured yet. Do not assume `npm test` exists.
- If adding tests, also add scripts and brief usage notes in [README.md](README.md).

## Change Discipline

- Keep changes scoped to the user request.
- Avoid introducing dependencies unless they are necessary for the requested outcome.
- If you change developer workflow, update [README.md](README.md) in the same change.
