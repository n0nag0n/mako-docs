# Installation

--------------------------------------------------------

* [Requirements](#requirements)
* [Setup](#setup)
* [Get started](#get_started)
* [Updating](#updating)

--------------------------------------------------------

<a id="requirements"></a>

### Requirements

* PHP 8.0.0 or higher *
* `ext-json`
* `ext-mbstring`

If you plan to use the database library then you'll also need to install `ext-pdo`.

\* Tested on PHP 8.0, 8.1 and 8.2

--------------------------------------------------------

<a id="setup"></a>

### Setup

Installing Mako is easy and can be with done in a few simple steps thanks to [composer](https://packagist.org).

First you'll have to create a new project:

```
composer create-project mako/app <project name>
```
{.language-none}

Next you'll have to make the `app/storage/*` directories writable (command my vary depending on your system):

```
chown www-data:www-data -R app/storage
```
{.language-none}

> Note that only the most essential [services](:base_url:/docs/:version:/getting-started:dependency-injection#services) are enabled by default. Enable the ones that you need by uncommenting them in the `app/config/application.php` configuration file.

--------------------------------------------------------

<a id="get_started"></a>

### Get started

Mako includes a simple development server which can be started with the following command:

```
php app/reactor server
```
{.language-none}

Open `http://localhost:8000` in your browser of choice and you're ready to start coding!

> The included development server is great when getting started and for quick prototyping but your should probably use a <abbr title="virtual machine">VM</abbr> or Docker setup that closely resembles your production environment for advanced projects.

--------------------------------------------------------

<a id="updating"></a>

### Updating

Mako and all your other dependencies can easily be updated when a new patch release is made available using the following command:

```
composer update
```
{.language-none}

If you want to bump the Mako version (e.g. from `9.0.*` to `9.1.*`) then you'll have to update your `composer.json` file before running the update command.

> Some releases might require some minor code changes. These will be documented in the upgrade guides.
{.warning}
