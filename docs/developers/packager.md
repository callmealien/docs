# OpenSpending Packager

The OpenSpending Packager is a Javascript app that provides data validation, modeling, and publishing capabilities for OpenSpending.

Using the Packager, users start with a raw data source (a CSV file) and follow the required steps to get this data into OpenSpending.

## Features

- Validate tabular data sources for good structure and a consistent schema.
- Model the data into a Fiscal Data Package.
- Provide additional meta data that gives the data context.
- Download the created `datapackage.json` descriptor, or publish the whole data package directly to OpenSpending.

## Requirements

You need to have a recent version of Node.js (v5 and above) to run the Packager.

If you are not too familiar with Node, do not worry about that. The Packager is almost completely a frontend Javascript app, with Node.js providing a simple shell and some conveniences for routing and setting environment variables.

The UI is written with [Angular 1](https://angularjs.org).

## Installation

The Packager can be installed as a component of the Platform, or as a stand alone component.

**Which installation method should you choose?**

- If your goal is to get a full instance of OpenSpending running, then go ahead with the platform installation.
- If you just want to hack on the Packager (Suggest new features! Fix bugs!), or even run your own Packager against a remote OpenSpending platform, then follow the standalone install.

If the options are confusing, then go ahead with the standalone install. By default, it runs against the Open Knowledge International instance of OpenSpending, so you'll immediately have lots of data to interact with.

### Platform install

Follow the instructions for installing a development environment for the [OpenSpending platform here](./platform/).

### Standalone install

Follow these steps to get the Packager running:

```
# get the code
git clone https://github.com/openspending/os-packager.git

# install dependencies
npm install

# build the frontend assets
npm run build

# run the tests
npm test

# run the server
npm start

# load the app in your default browser
open http://127.0.0.1:5000
```

Based on the default configuration of the Packager, you can now work with the entire OpenSpending database hosted by Open Knowledge International from your local machine. If you want to point to a different OpenSpending instance, configure your environment variables accordingly based on the details below.

### Customisation

#### Environment variables

OpenSpending Packager is configured using environment variables. The following variables are available:

- `OS_PACKAGER_CONDUCTOR_HOST`: the URL of the domain that the conductor app is served from.
- `OS_PACKAGER_BASE_PATH`: The base path for the app, needed to serve Packager from a subdirectory instead of a subdomain.

### Contributing code

Found a bug? Got neat way to refactor an existing code path? Bursting with ideas to make the Packager more awesome?

We *can't wait* to see your contributions. Here are a few things that will help:

- All open issues for the Packager [can be found here](http://github.com/openspending/openspending/issues), labeled "Packager". If you are working on an existing issue, please let us know by commenting on an issue. Likewise, if you are working on something new, open an issue to let us know.
- We follow a set of [coding standards](https://github.com/okfn/coding-standards), and we have simple examples of those coding standards implemented for [Python](https://github.com/okfn/oki-py) and [Javascript](https://github.com/okfn/oki-js). Please do read before starting.

If anything is unclear, or you just want to talk with other people working on OpenSpending, then catch us on [Gitter.im](http://gitter.im/openspending/chat).
