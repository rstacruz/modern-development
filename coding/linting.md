# Linting

<figure class='-bordered -w60'>
<img src='../images/lint-error.png' alt='Lint error example'>
</figure>

Linters are tools that enforce source code writing style based on a set of rules. It helps impose coding styleguides in an automated way. A linter will check decisions such as:

- Tabs or spaces for indentation
- Naming of variables and functions
- Use of whitespace
- Patterns to use and to avoid

It's important to keep your coding style consistent: even if it's mostly subjective, a consistent coding style helps keep developer sanity.

## Automated linting

Linting should be part of your automated test suite. This lets you catch style violations before pull requests are merged. This is especially useful for open source projects that welcomes irregular contributors, but even private projects can benefit from this. Here's an example using Travis CI:

```yaml
# Example .travis.yml configuration to run CS
# and JavaScript linting
scripts:
  - npm test
  - npm run stylelint
  - npm run eslint
```

## Why use a linter

Linting helps reviewers by catching style violations in automated tests so they don't have to. This means less effort needed for reviewing, and instant feedback for contributors.

<figure class='-w80'>
<img src='../images/github-build-failure.png' alt='GitHub build failure example'>
<figcaption>Linting prevents merging when style issues aren't fixed.</figcaption>
</figure>

Linters also catch syntax errors. This is useful for assets like JavaScript and CSS which may not be compiled as part of the test suite.

## Choose a coding style

There are many established styleguides and linter presets. Pick one and customize it if preferred. It doesn't matter which you choose, what's important is that your team has an authoritative set of rules that are enforced by a linter. This prevents petty "bikeshedding" arguments within your team.

- JavaScript: [Standard](http://standardjs.com/), [XO](https://www.npmjs.com/package/xo)
- CSS: [Config standard](https://www.npmjs.com/package/stylelint-config-standard)

## Linter examples

- [Stylelint](http://stylelint.io/) for CSS
- [Eslint](http://eslint.org/) for JavaScript
- [Rubocop](https://github.com/bbatsov/rubocop) for Ruby
- [Credo](https://github.com/rrrene/credo) for Elixir
