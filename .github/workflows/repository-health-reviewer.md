---
on:
  push:
    branches:
      - main

  workflow_dispatch:

permissions:
  contents: read

safe-outputs:
  create-issue:
    max: 1

---

# Repository Health Reviewer

Review the repository after every push to the main branch.

Analyze the repository and identify:

- Whether tests are present
- Whether documentation is present
- Potential code quality problems
- TODO, FIXME, and DEBUG markers
- Obvious missing or incomplete areas
- Potential risks in the latest changes

Create one GitHub issue containing:

# Repository Health Report

## Summary

Provide a short summary of the repository health.

## Tests

State whether tests are present and identify important gaps.

## Documentation

State whether useful documentation is present.

## Code Quality

Identify obvious code quality concerns.

## Warning Markers

Report TODO, FIXME, DEBUG or similar markers.

## Recommendations

Provide 3-5 practical recommendations.

Do not modify source code.

Only create the GitHub issue described above.