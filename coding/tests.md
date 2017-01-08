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

In our Git workflow that relies on branching and merging, automated tests are part of the code review process. By maintaining a healthy test suite in a project, we can ensure that the main branches of the project, `master` and `develop`, are always in a working state.

## Unit vs. integration tests

Tests will commonly be either a *unit test* that tests one thing, or an *integration test* that tests many things. Here's the same behavior tested in two different ways:

```rb
# Unit test example: tests the model
test 'Article publishing' do
  article.publish!
  expect(article.published_at).to eq Time.now
end
```

```rb
# Integration test example: tests your router,
# controller, view, and model all at once
test 'Article publishing' do
  post '/articles/my-draft-article/publish'
  expect(article.published_at).to eq Time.now
end
```

In web development, unit tests are often written for models and services, while integration tests are for controllers.

## Smoke tests

A smoke test is a very shallow integration test. It usually just tries something and expects no errors to happen. The name comes from testing electronics to check if turning a device on produces smoke. In web development, it usually means just visiting a path and checking for errors.

```rb
test 'No fires happen' do
  visit '/article/my-article'
  expect(response.code).to eq 200
end
```

The simple test above will already check for a lot of things:

- Any errors in the view templates
- Any model or controller errors
- Middleware in the app server

<details>
<summary>See also...</summary>

<ul>
<li><a href='https://en.wikipedia.org/wiki/Test-driven_development'>Test-driven development</a> (wikipedia.org)</li>
</ul>
</details>

> **Next:** [Why do we write tests?](why_test.md)
