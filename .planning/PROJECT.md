# Project: md2blogger Vulnerability Fix

## Purpose of Fork
This fork was created to address a critical vulnerability and update dependencies to ensure the security and stability of the tool.

## Milestone: Resolve tmp Vulnerability
### Goals
- Resolve the 4 low-severity vulnerabilities reported by `npm audit` in the `tmp` transitive dependency.
- Remove `md2blogger` from `devDependencies` to prevent self-referencing issues.
- Maintain CLI functionality.

## Context
A CLI tool that helps the maintenance of a blog hosted on Blogger.
The project currently reports 4 low-severity vulnerabilities during `npm install`.


## Objectives
- Fix 17 vulnerabilities (7 low, 4 moderate, 5 high, 1 critical) reported by `npm install`.
- Ensure the project remains functional after dependency updates.

## Technical Details
- **Language:** JavaScript (Node.js)
- **Dependencies:** axios, chalk, commander, express, http-terminator, image-to-base64, inquirer, js-yaml, markdown-it, markdown-it-container, open.
- **Vulnerability discrepancies:** `npm audit` on current environment reports 4 low vulnerabilities, but the user reports 17.

## Assumptions
- The vulnerabilities are in the dependencies or their transitive dependencies.
- `npm audit fix` may resolve some or all issues.
- Major version updates may be required for some dependencies.
