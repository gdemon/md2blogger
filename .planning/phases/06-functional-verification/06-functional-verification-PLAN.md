# Phase 6 Plan: Functional Verification

Verify the tool remains functional after all dependency updates and vulnerability fixes.

## Objectives
- Confirm `md2blogger --help` works as expected.
- Verify basic markdown conversion functionality.
- Ensure authentication logic starts correctly (without necessarily completing a full Blogger post).
- Verify the regex fix in `src/conversion.js`.

## Tasks
1. **CLI Help Command Verification:**
   - Run `node src/cli.js --help` and verify output.
2. **Sample Conversion Verification:**
   - Use `resources/sample.md` to test the conversion logic.
   - Run `node src/cli.js --md resources/sample.md --url https://dummyblog.blogspot.com`.
   - Verify it handles the frontmatter and images correctly.
3. **Regex Fix Verification:**
   - Specifically check if `src/conversion.js` correctly handles image paths with the previous regex update.
4. **Final dependency check:**
   - Confirm no runtime errors from major version updates of `chalk`, `commander`, etc.

## Success Criteria
- `md2blogger --help`: Success.
- Sample conversion: No runtime crashes, correctly identifies images and frontmatter.
- Clean `npm audit` report.
