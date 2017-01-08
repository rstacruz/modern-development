# The staging system

<figure class='-w60'>
<img src='../images/staging-site.png' alt='yoursite.com and staging.yoursite.com illustration'>
</figure>

In web development, a staging server is a separate site where the latest development version is always available. It's completely separate from your production system. This lets your developers, testers, and stakeholders try the latest changes without having to touch the production system.

## Setting up a staging system

The most ideal staging setup is a system that's exactly like your production system: same type of server, same type of databases, but hosted separately. You can use a cheaper configuration, since less people will be using your staging.

Most projects start with using [Heroku](http://www.heroku.com/) for their staging system. It's free, it supports almost every programming language, and setting a new website up takes 2 commands (see Heroku's [documentation](https://devcenter.heroku.com/start)).

## Automating staging updates

<figure class='-bordered -w60'>
<img src='../images/semaphore-deploy-commands.png' alt='Deploy commands example'>
<figcaption>Example deploy script in Semaphore.</figcaption>
</figure>

A typical CI setup is have the following auto-deployments done:

- Auto deploy passing tests in branch `develop` to your staging server.
- Auto deploy passing tests in branch `master` to your production server.

When tests pass in a given branch, an auto deploy script will simply run certain commands.

<!-- <figure class='-bordered'>
<img src='../images/semaphore-deployment-example.png' alt='Semaphore screenshot'>
<figcaption>Setting up auto deployment in Semaphore.</figcaption>
</figure> -->


## Seeding a staging system

The data in a staging system is completely different from your production system. It will probably start off as blank. You'll need some test data in your staging server to make it look like a production server. Making dummy data is a process called seeding. Seeding generates some dummy users, articles, and whatever your project needs to get it to a state where it "looks" like a production system.

To do this, you'll make a seed script in your project invoked by a certain command. In Rails projects, that's:

```sh
# Invokes db/seeds.rb
bundle exec rails db:seed
```

> **Next:** Track your code's health with [code coverage reporting](coverage.md).
