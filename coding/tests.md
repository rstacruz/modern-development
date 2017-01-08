# Test-driven development

<figure class='-bordered -p80'>
<img src='../images/tdd-flowchart.png' alt='TDD flowchart'>
</figure>

Test-driven development, or TDD, means writing tests along with your code. It's not about writing tests after you're done, but making testing a habit as part of your development process.

  - Tests should be written alongside your implementation.
  - New features need to have new tests for it.
  - Features can't be merged unless tests pass.

## What to test

A healthy code base has tests written in this priority (most important to least):

  1. Unit tests
  2. Smoke tests
  3. Integration tests

Units tests are easy to make and are a natural part of the process of writing models. Smoke tests are small and also easy to make. Integration tests are larger and harder to maintain, so it's often more economical to prioritize writing smaller unit tests.

## In the Git workflow

The main branches `master` and `develop` must always be in a working state. Pull requests can't be merged until their tests pass.

> **Next:** What are [unit, integration, and smoke tests](test_types.md)?
