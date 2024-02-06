<img width="1440" alt="dashboard" src="https://github.com/maybe-finance/maybe/assets/35243/4910781f-4bea-4a3b-8fb6-21f314548c9d">

# Maybe: The OS for your personal finances

<b>Get involved: [Discord](https://link.maybe.co/discord) • [Website](https://maybe.co) • [Issues](https://github.com/maybe-finance/maybe/issues)</b>

_If you're looking for the previous React codebase, you can find it at [maybe-finance/maybe-archive](https://github.com/maybe-finance/maybe-archive)._

## Backstory

We spent the better part of 2021/2022 building a personal finance + wealth management app called, Maybe. Very full-featured, including an "Ask an Advisor" feature which connected users with an actual CFP/CFA to help them with their finances (all included in your subscription).

The business end of things didn't work out, and so we shut things down mid-2023.

We spent the better part of $1,000,000 building the app (employees + contractors, data providers/services, infrastructure, etc.).

We're now reviving the product as a fully open-source project. The goal is to let you run the app yourself, for free, and use it to manage your own finances and eventually offer a hosted version of the app for a small monthly fee.

## Moving from React/Next.js to Ruby on Rails

The original codebase we open-sourced in January 2024 was a React/Next.js/Express app. There were a substantial number of issues with that codebase, rooted in large part to the requirements for SOC2 and SEC compliance and our dependency on a number of third-party data providers. Not to mention that a lot of the tech has changed in the React world since 2021.

As we started digging into the changes that would be required to get the app fully up and running again, we realized we'd actually end up rewriting the vast majority of the app. So instead of doing that in an incredibly slow and painful way, we decided to start from scratch with a new codebase. Yes, that's risky. But so is trying to rebuild a complex app on a codebase that's 3 years old and wasn't originally built for the requirements we now have.

We're now building the app in Ruby on Rails. We realize that's a controversial choice, but we believe it's the right one for the project. Rails is a mature, stable, and well-documented framework that's been around for over 20 years built on a language that's been around for over 30 years.

From the start our focus with this is to make it as easy as possible for you to both contribute to and deploy the app, and this move to Rails is a big part of that.

## Local Development Setup

### Requirements

- Ruby >3 (see `Gemfile`)
- PostgreSQL >9.3 (ideally, latest stable version)

After cloning the repo, the basic setup commands are:

```sh
cd maybe
cp .env.example .env
bundle install
rails db:setup
bin/dev
```

And visit http://localhost:3000 to see the app. You can use the following credentials to log in (generated by DB seed):

Email: user@maybe.local
Password: password

For further instructions, see guides below.

### Setup Guides

#### Dev Container (optional)

This is 100% optional and meant for devs who don't want to worry about installing requirements manually for their platform. You can follow [this guide](https://code.visualstudio.com/docs/devcontainers/containers) to learn more about Dev Containers.

#### Mac

Please visit our [Mac dev setup guide](https://github.com/maybe-finance/maybe/wiki/Mac-Dev-Setup-Guide).

#### Linux

Please visit our [Linux dev setup guide](https://github.com/maybe-finance/maybe/wiki/Linux-Dev-Setup-Guide).

#### Windows

Please visit our [Windows dev setup guide](https://github.com/maybe-finance/maybe/wiki/Windows-Dev-Setup-Guide).

### Testing Emails

In development, we use `letter_opener` to automatically open emails in your browser. When an email sends locally, a new browser tab will open with a preview.

## Contributing

Before contributing, you'll likely find it helpful to [understand context and general vision/direction](https://github.com/maybe-finance/maybe/wiki).

Once you've done that, please visit our [contributing guide](https://github.com/maybe-finance/maybe/blob/main/CONTRIBUTING.md) to get started!

## Self Hosting

Our long term goal is to make self-hosting as easy as possible. That said, during these early stages of building the product, we are focusing our efforts on development.

We will update this section as we get closer to an initial release.

Please see our [guide on self hosting here](https://github.com/maybe-finance/maybe/wiki/Self-Hosting-Setup-Guide).

## Repo Activity

![Repo Activity](https://repobeats.axiom.co/api/embed/7866c9790deba0baf63ca1688b209130b306ea4e.svg "Repobeats analytics image")

## Copyright & license

Maybe is distributed under an [AGPLv3 license](https://github.com/maybe-finance/maybe/blob/main/LICENSE). "Maybe" is a trademark of Maybe Finance, Inc.
