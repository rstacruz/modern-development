# Readme files

Every project should have a `README.md` file in their Git repository. It should contain everything anyone ever needs to get started working on the project.

- External links (Trello, JIRA, Slack, and so on)
- Required software and how to install them
- Setting up a development environment
- Deployment instructions
- Running tests

## The purpose

When a new developer joins the team, they should be able to get by by simply telling them to "read the readme file". This helps the project in many ways:

- Makes it easy for people to join the team.
- Helps out team members when moving to new laptops.

Be sure to maintain the Readme file. Things may change and get added to the project that the Readme may need to be updated. Don't let it stagnate, you'll never know when you'll need it!

## Example readme

This is a bare example that manages to cram everything in the list above in just a few sections.

> <h4 class='quote-heading'>README.md example</h4>
>
> ## Requirements
>
> * Ruby 2.3
> * Redis 2.3
> * PostgreSQL 9.5
> * Bundler (`gem install bundler`)
>
> For OSX, we recommend you install via:
>
> * [Homebrew](http://brew.sh/)
> * Ruby via [RVM](https://rvm.io/)
> * Redis via Homebrew (`brew install redis`)
> * Postgres via Homebrew (`brew install postgres`)
>
> ## Setting up
>
> Install dependencies via Bundler and npm:
>
> ```bash
> git checkout https://github.com/x/my_project.git
> cd my_project
>
> bundle
> npm install
> ```
>
> Run a Rails development server:
>
> ```bash
> bundle exec rails s
> ```
>
> ## Running tests
>
> Tests are managed via RSpec.
>
> ```bash
> bundle exec rspec
> ```
>
> ## Deployments
>
> Deployments are managed via SemaphoreCI using Capistrano. `develop` is automatically deployed to [staging.oursite.com](#), while `master` is auto-deployed to [oursite.com](#) production. To manually invoke a deployment, use:
>
> ```bash
> bundle exec cap staging deploy     # staging.oursite.com
> bundle exec cap production deploy  # oursite.com
> ```
>
> ## Also see
>
> * [Slack team](#) for communication
> * [Trello board](#) for stories and bug reports
> * [SemaphoreCI](#) for tests and deployments

<br>

> **Next:** [Go back](../toc/README.md)
