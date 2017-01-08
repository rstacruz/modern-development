# Using Slack

A team should have these channels for every project:

- A channel where everyone is, including developers and stakeholders (usually `#general`).
- A developer-only channel (usually `#dev`).
- Notifications for project tracker updates (usually `#issues`).

## General channel

> <h4 class='quote-heading'>#general</h4>
>
> *Stakeholder:* Good morning guys, are we still on track for sprint 5?<br>
> *Daphne:* Yep! We should be about 80% there right now.

This is the default channel for most discussions. Collaborating with stakeholders happens here. Most conversations should happen here, unless they happen to be too technical, in which case they should be in `#dev`.

## Developer channel

> <h4 class='quote-heading'>#dev</h4>
>
> *Fred:* Can you guys take a look at PR #283? I need a review<br>
> *Velma:* Hold on, let me take a look at it.

Have a channel where only developers are present, without any stakeholders. This is where everyday tech-related discussions will happen. Banter in this channel is usually not relevant to stakeholders, so it's best to leave them out so not to overwhelm them.

## Temporary channels

> <h4 class='quote-heading'>#_facebook-campaign</h4>
>
> *Marketer:* We need a new landing page<br>
> *Fred:* We're on it. What do you need?

Create new channels for discussion threads, and archive them when you're done. We usually name these with an underscore, such as `#_feature`. This lets certain discussions happen separately from everyday banter, keeping its logs clean. It also prevents overwhelming people by leaving out those who may not be involved.

## Project tracker channel

> <h4 class='quote-heading'>#issues</h4>
>
> *GitHub:* Shaggy submitted pull request #283: *Homepage: fix responsive issues*<br>
> *Trello:* Scooby added a new card: *Facebook landing pages*

Integrate your project management tool (eg, Trello) and GitHub's pull requests into a channel such as `#issues`. Don't talk in this channel, take discussions to `#general` instead since conversations are hard to track among notifications.

## Other notifications

Also consider adding notifications for other services. This largely depends on the nature of your project. Here are some ideas:

- `#analytics` for website analytics (eg, Google Analytics)
- `#support` for customer support tickets (eg, Intercom)
- `#ding` for sales notifications
