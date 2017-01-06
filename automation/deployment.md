# Automated deployments

Before you can use a CI for continuous delivery, you'll need to set up a deploy automation tool.

A modern project needs to have a simple set of commands to magically update your servers. Contrast this to legacy projects, where deployment may involve manually transfering files and using a browser to invoke certain commands. These tasks need to be automated so they can be repeatable and protected from human errors.

## Example

For websites hosted on [Heroku](https://www.heroku.com/), their platform already takes care of deploy automation for you. To update a Heroku website, you simply need to do a `git push`:

```sh
# Deploy your app into Heroku's hosting platform
git push heroku master
```

In other cases, you'd have to use other tools to take care of this for you. For Ruby projects, [Capistrano](http://capistranorb.com/) is a popular utility exactly for this purpose. A typical Ruby/Capistrano project would be deployed like so:

```sh
# Deploy your app using Capistrano
bundle exec cap production deploy
```

## How to set up deployments

There are many different tools for this for many different programming languages. Some popular ones include:

- [Fabric](http://www.fabfile.org/) (Python)
- [Capistrano](http://capistranorb.com/) (Ruby)
- [Shipit](http://www.fabfile.org/) (Node.js)
- [Edeliver](https://github.com/boldpoker/edeliver) (Elixir and Erlang)

It doesn't matter which solution you pick, as long as your project's deployments are easy, automated, and reliable.

> **Next:** Use your CI to [automatically update servers](#).
