# Roadmap: Vulnerability Fixes & Enhancements

## Phase 1: Research & Audit Discrepancy (COMPLETED)
- Analyzed `npm audit` and `npm outdated` outputs.
- Confirmed discrepancy between user's report (17) and current environment (4).

## Phase 2: Dependency Updates (COMPLETED)
- Updated `inquirer` to `13.x` to fix transitive vulnerabilities.
- Updated `chalk`, `commander`, `express`, and `open` to latest versions.
- Ran `npm audit fix --force` and achieved 0 vulnerabilities (temporarily).

## Phase 3: Verification & Functional Testing (COMPLETED)
- Verified CLI basic functionality (`md2blogger --help`).
- Fixed a cross-platform regex bug in `src/conversion.js`.

## Phase 4: Milestone 1 Finalization (COMPLETED)
- Updated project documentation and state.

## Phase 5: Resolve Transitive Vulnerability (COMPLETED)
- Remove self-referencing `md2blogger` from `devDependencies`.
- Resolve the `tmp` transitive vulnerability.
- Re-run `npm install` and `npm audit`.


## Phase 6: Functional Verification (COMPLETED)
- Verify `md2blogger --help`.
- Run a sample markdown conversion with the updated dependencies.

