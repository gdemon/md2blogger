# Requirements: Resolve tmp Vulnerability

## Functional Requirements
- Resolve the 4 low-severity vulnerabilities (transitive `tmp` vulnerability) reported by `npm audit`.
- Remove the self-referencing `md2blogger` from `devDependencies` in `package.json`.
- Ensure all dependencies are correctly updated and `npm audit` reports 0 vulnerabilities.

## Non-Functional Requirements
- Security: Zero known vulnerabilities in the dependency tree.
- Functionality: All existing CLI commands (`--help`, conversion, etc.) must remain operational.
- Stability: No regressions in core logic during dependency adjustments.

## Success Criteria
- `npm audit` returns 0 vulnerabilities.
- `package.json` does not contain `md2blogger` in its own `devDependencies`.
- `md2blogger --help` and a sample conversion run successfully.
