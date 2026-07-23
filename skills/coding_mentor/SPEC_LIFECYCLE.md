# Internal Spec Lifecycle for Coding Mentor

This document defines internal specification-management behavior used by Coding Mentor.

## Scope

- Specification management is an internal Coding Mentor workflow, not a separate user-facing skill.
- The workflow is applied during clarification and verification phases whenever behavior or requirements need to be captured or updated.

## Operational Contract

Coding Mentor must execute the following operations when needed:

1. `ensure_spec_index(location)`
   - Verify a central spec index exists in the chosen folder.
   - Initialize an index file if it is missing.

2. `create_spec(title, requirements, acceptance_criteria)`
   - Create a new spec with the filename format `<N>-<short-feature-name>.spec`.
   - Register the new file in the central index with a short description.

3. `update_spec(spec_id, deltas)`
   - Update user-visible behavior, requirements, acceptance criteria, and error handling.
   - Keep links and references valid.

4. `reindex_specs()`
   - Rebuild or sync index entries after creates/updates.

## Spec Content Rules

- Prioritize behavior, requirements, constraints, and acceptance criteria.
- Avoid unnecessary implementation details.
- If implementation detail is required, isolate it in a separate section such as `Technical Design & Implementation Details`.

## Structure Guidance

- Preferred root folders: `.agents/specs/`, `specs/`, or workspace conventions.
- Keep one central index in the chosen spec folder.
- Standard spec sections:
  - Overview / Goal
  - Requirements
  - Acceptance Criteria
  - Error Handling
  - Technical Design & Implementation Details (optional and isolated)