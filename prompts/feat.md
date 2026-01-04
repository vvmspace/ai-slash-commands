# feat - add a new feature

Act as a senior software engineer to add a new feature to the repository.

### 0) Inputs and constraints

* Feature request (user description)
* Repo context (structure, stack, conventions, CI)
* Constraints (deadline, “no refactors”, compatibility, platforms, versions)

If critical info is missing, ask only the minimum set of questions required to proceed. Otherwise, make reasonable assumptions and clearly list them.

### 1) Define the feature

Produce:

* A 1-2 sentence goal statement
* Primary user flows (happy path + 2-3 important edge cases)
* Definition of Done (clear acceptance criteria)
* Constraints and compatibility notes (APIs, data, platforms, versions)

### 2) Codebase reconnaissance

Before editing:

* Identify where this feature should live (files/modules)
* List integration points (API/UI/CLI/config/DB)
* Call out risks (breaking changes, migrations, flags, performance, security)

### 3) Implementation plan

Create a small-step plan:

* What changes by file/module
* New entities/interfaces/types/endpoints/tables (if any)
* Minimal incremental approach: skeleton first, then expand
* Rollback strategy and/or feature flag if risk is non-trivial

### 4) Implement

Make changes carefully:

* Follow existing architecture and style
* Avoid duplication; extract shared logic
* Use clear names; add comments only when they add real value
* Preserve backward compatibility unless explicitly instructed otherwise
* Keep diffs focused; avoid unrelated refactors

### 5) Tests

* Add/update tests (unit/integration) for key flows, if tests are present in the project.
* Include regression coverage for the behavior this feature is meant to address (when applicable)
* If tests are difficult, explain why and provide an alternative verification plan (smoke/e2e/manual checklist)

### 6) Documentation and developer experience

* Update README/docs/examples as needed
* Document new config/env variables and defaults
* Add “How to verify locally”: commands and a couple of usage examples

### 7) Final summary

End with:

* What changed (brief)
* Files touched (grouped by purpose)
* Commands to verify (lint/test/build/run)
* Known limitations / follow-ups (if any)
