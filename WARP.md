# WARP.md

This file provides guidance to WARP (warp.dev) when working with code in this repository.

Project overview
- Name: DevJobs
- Source: README.md
- Purpose: Learning project from a FullStack Bootcamp (midudev) while evaluating Warp. Goals include improving skills in JavaScript, CSS, HTML, React, and Node; and exploring CI/CD, testing, DevOps, and Docker.

Repository layout (high level)
- docs/: Project documentation (e.g., docs/overview.md for goals, scope, ADRs, and milestones)
- src/: Application source code (currently empty aside from a placeholder)

Architecture summary
- This repository is currently a skeleton. No application modules, build toolchain, or test framework are present yet. Expect the following to evolve:
  - Application code will live in src/.
  - Documentation and decisions (including ADRs) will live in docs/.
  - Tooling (build/lint/test) is not yet configured; once introduced, prefer exposing developer commands via package.json scripts (or equivalents) and document them here.

Common commands (current state)
- Build: Not configured yet.
- Lint: Not configured yet.
- Tests: Not configured yet.

Once tooling is added, prefer the following conventions so future agents can operate consistently:
- Node/JS scripts (if a package.json is added):
  - List available scripts: npm run
  - Build: npm run build
  - Lint: npm run lint
  - Test (all): npm test
  - Test (single, if using Jest): npx jest path/to/test.spec.ts -t "Test name"
  - Test (single, if using Vitest): npx vitest run path/to/test.spec.ts -t "Test name"
- If a different stack is adopted (e.g., Python/Go), add the corresponding build/lint/test commands here and keep this section up to date.

Important docs to consult first
- README.md: High-level goals and current structure
- docs/overview.md: Where to capture scope, ADRs, requirements, and milestones

Rules and external agent files
- No CLAUDE.md, Cursor rules (.cursor/rules/ or .cursorrules), or Copilot instruction files detected at this time.

Maintenance notes for future changes
- Whenever new tooling is introduced (build, lint, tests, CI), update the Common commands section with exact commands (including single-test examples) and add a brief note on where configs live (e.g., jest.config.ts, vitest.config.ts, eslint config, tsconfig.json).
- If the architecture evolves (e.g., introducing a server/client split, monorepo, or services), add a short map of top-level modules and how they interact at a high level.
