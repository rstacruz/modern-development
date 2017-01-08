# Continuous integration

<figure class='-s60 -shadow'>
<img src='../images/travis-ci-example.png' alt='Travis CI screenshot'>
</figure>

A modern development pipeline will need a continuous integration (CI) service. A CI service lets you run tasks whenever your project gets updated. These are usually used to automatically run tests in your project. CI services are used to automate:

- Running unit and integration tests
- Deploying to websites
- Generating builds (eg, mobile and desktop apps)

## Popular CI services

There are many CI services available today. Most of them offer free plans for open source projects, with paid plans available for private projects. Here's a selection of some of the more popular ones at time of writing:

- [Travis CI](https://travis-ci.org/) is popular among open source projects.
- [Appveyor](https://www.appveyor.com/) is useful for Windows projects.
- [Codeship](https://codeship.com/) specializes in Docker.
- [GitLab](https://about.gitlab.com/gitlab-ci/) offers a CI service with its platform.
- [Semaphore](http://semaphoreci.com/)
- [Circle](http://circleci.com/)

It doesn't really matter which CI solution you pick. What's important is that you use a CI to automate your testing and deployments. What you choose typically depends on the features you need and your budget.

> **Next:** Let's use a CI to [automate our tests](testing.md).
