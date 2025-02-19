# Solidus Starter Frontend
[![CircleCI](https://circleci.com/gh/solidusio/solidus_starter_frontend.svg?style=shield)](https://circleci.com/gh/solidusio/solidus_starter_frontend)

`solidus_starter_frontend` is a new starter storefront for [Solidus][solidus].

This project aims to deliver a modern, minimal, semantic, and easy to extend
codebase for a more efficient bootstrapping experience.

**DISCLAIMER**: some Solidus extensions (the ones that depend on Solidus
Frontend) will not work with this project because they rely on defacing some
views items that don't exist here.

## Objectives

We aim to deliver:

- a minimal, semantic and accessible HTML skeleton
- a reusable component based architecture
- simple SASS styling strictly based on BEM
- the elimination of jQuery as a dependency by rewriting frontend functionality
  in vanilla JavaScript

All of this while keeping and improving on the functionality of the current
[Solidus][solidus] frontend subcomponent.

## Installation

Just run:

```bash
rails new store --skip-javascript
cd store
bundle add solidus
bin/rails generate solidus:install --frontend=solidus_starter_frontend
```

That will create a new Solidus application with SolidusStarterFrontend as its
storefront.

Please note that [Solidus Auth Devise](https://github.com/solidusio/solidus_auth_devise)
will also be added to your application as it's required by SolidusStarterFrontend.

## Considerations

The installation of Solidus Starter Frontend will copy the frontend views,
assets, routes, controllers, and specs to your project. You can change easily
anything that we created; this gives you a lot of freedom of customization.

Note that since the Solidus Starter Frontend is a Rails
application template, it doesn't have the capability to automatically update
your storefront code whenever the template is updated.

It is not possible right now to generate a new Rails app with the template, i.e.
run `rails new --template=URL` since the template expects Solidus to be
installed on the app.

In addition, please note that it will add Solidus Auth Devise frontend
components to your app. At the moment, you will need to manually remove the gem
and its frontend components if you don't need them.

## Security updates

To receive security announcements concerning Solidus Starter Frontend, please
subscribe to the
[Solidus Security mailing list](https://groups.google.com/forum/#!forum/solidus-security).
The mailing list is very low traffic, and it receives the public notifications
the moment the vulnerability is published. For more information, please check out
https://solidus.io/security.

## Development

For information about contributing to this project please refer to this
[document](docs/development.md). There you'll find information on tasks like:

* Testing the extension
* Running the sandbox
* Updating the changelog
* Releasing new versions
* Docker development

## About
[![Nebulab][nebulab-logo]][nebulab]

`solidus_starter_frontend` is funded and maintained by the [Nebulab][nebulab]
team.

We firmly believe in the power of open-source. [Contact us][contact-us] if you
like our work and you need help with your project design or development.

[solidus]: http://solidus.io/
[nebulab]: http://nebulab.it/
[nebulab-logo]: http://nebulab.it/assets/images/public/logo.svg
[contact-us]: http://nebulab.it/contact-us/

## License
Copyright (c) 2020 Nebulab SRLs, released under the New BSD License.
