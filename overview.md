## Overview
[Data Collection](#package-managers)
* [Package Managers](#package-managers)
* [Repositories](#repositories)
* [Licenses](#licenses)

[Architecture](#architecture)
* [Diagram](#architecture)
* [Components](#components)

### Package Managers
Everything in Libraries.io begins with [package managers](/packagemanagers.md). On a regular basis, background tasks find new or updated libraries from each of those packages managers. Libraries cannot be added to the system unless they exist on one of those package managers.

#### Projects, Versions and Dependencies
Each library is stored in the [Project](https://github.com/librariesio/libraries.io/blob/master/app/models/project.rb) table. If a library's package manager supports published version numbers, each new version is stored in the [Version](https://github.com/librariesio/libraries.io/blob/master/app/models/version.rb) table; and if the package manager supports library dependencies, then they are recorded in the [Dependency](https://github.com/librariesio/libraries.io/blob/master/app/models/dependency.rb) table.

### Repositories
Libraries.io will then augment package manager data with data from a Repository if one is referenced in the package manager. GitHub repositories will be downloaded and stored in the [Repository](https://github.com/librariesio/libraries.io/blob/master/app/models/repository.rb) table, on creation a background Sidekiq task is kicked off to download related information from GitHub including:

- [Readme](https://github.com/librariesio/libraries.io/blob/master/app/models/readme.rb)
- [Tags](https://github.com/librariesio/libraries.io/blob/master/app/models/github_tag.rb)
- [Contributors](https://github.com/librariesio/libraries.io/blob/master/app/models/github_contribution.rb)
- Owner ([GitHub user](https://github.com/librariesio/libraries.io/blob/master/app/models/github_user.rb) or [GitHub Org](https://github.com/librariesio/libraries.io/blob/master/app/models/github_organisation.rb))
- Source repository (if it's a fork)
- [Dependency Manifests](https://github.com/librariesio/libraries.io/blob/master/app/models/manifest.rb)

Some package managers that don't have a concept of published versions (like Go and Bower), often they will fall back to using tags from a source repository if available, Libraries.io attempts to use GitHub tags as a fallback for all package managers that don't provide version information.

### Licenses
License names are ran through [SPDX](https://github.com/librariesio/spdx). This standardises the many different ways of writing the same licenses into a single version, which is then used for filtering in search and listing on https://libraries.io/licenses. A library can have multiple licenses as it may contain other libraries with conditions that are enforced upward. If a project doesn't have any license data from the package manager then it will fall back to using the (singular) Repository license.

If a project has a non-standard or commercial license it's currently normalized to "Other" and is not indexed in search.

## Architecture
Libraries.io is made up of a number of micro-services that work together. The following diagram provides a high-level overview:

![Overview of Libraries.io architecture](infrastructure.png "Libraries.io Architecture")

## Components

The main bits are:

### Core Web App

* [Libraries.io](https://github.com/librariesio/libraries.io) The main website and the data store.

### Parser services
* [mix-deps-json](https://github.com/librariesio/mix-deps-json) Elixir parser for Hex dependency manifests
* [clojars json](https://github.com/librariesio/clojars-json) Convert clojars.org data to JSON
* [Carthage Parser](https://github.com/librariesio/carthage_parser) Web service for parsing Carthage manifests
* [Yarn Parser](https://github.com/librariesio/yarn-parser) Web service for parsing yarn.lock manifests
* [Pydeps](https://github.com/librariesio/pydeps) Web service for calculating dependencies for python modules via pip
* [Cocoapods API](https://github.com/librariesio/cocoapods-api) Web service for indexing cocoapods specs repo
* [gradle parser](https://github.com/librariesio/gradle-parser) Web service for parsing gradle dependencies
* [npm-update-stream](https://github.com/librariesio/npm-update-stream) Web service for indexing npm update stream

### The API
[Firehose](https://github.com/librariesio/firehose) Server Sent Events API for Libraries.io releases

### Libraries
* [Bibliothecary](https://github.com/librariesio/bibliothecary) Parses manifest files
* [Gemnasium Parser](https://github.com/librariesio/gemnasium-parser) An improved fork of gemnasium-parser
* [Semantic Range](https://github.com/librariesio/semantic_range) node-semver written in Ruby for comparison and inclusion of semantic versions and ranges.
* [SemanticInterval](https://github.com/librariesio/semantic_interval) Turns Interval range syntax into Semantic Version range syntax
* [License Compatibility](https://github.com/librariesio/license-compatibility) Checks compatibility between different licenses from SPDX
* [SPDX](https://github.com/librariesio/spdx) Standardises licenses
* [Pictogram](https://github.com/librariesio/pictogram) Logos for programming languages and package managers
* [Package Managers](https://github.com/librariesio/package-managers) Metadata about every package manager that Libraries.io supports

### GitHub Firehose
* [Github Firehose](https://github.com/librariesio/github-firehose) Server-sent Events firehose of the GitHub public timeline
* [Dispatch](https://github.com/librariesio/dispatch) Dispatch events from various sources into Libraries.io job queue

### Webhooks
* [Lib2Issues](https://github.com/librariesio/lib2issues) Create GitHub Issues from Libraries.io webhooks
* [Travis Rebuilder](https://github.com/librariesio/travis-rebuilder) Rerun travis-ci tests after any dependency is updated
* [Sentinel](https://github.com/librariesio/sentinel) Automated dependency updates for Node.js projects

### Bots
* [Just Open Sourced](https://github.com/librariesio/justopensourced) Tweeting whenever a repo is open sourced on GitHub
* [Libby](https://github.com/librariesio/libby) Libraries.io hubot

### Firehose
* [Firehose Stream](https://github.com/librariesio/firehose-stream) Live streaming visualization of Libraries.io releases

### Tools
* [Required files (library)](https://github.com/librariesio/required_files) Ensures that certain files exist in all our repo's
* [Required files](https://github.com/librariesio/required-files) Files that should exist in every Libraries.io repository
* [libsearch](https://github.com/librariesio/libsearch) CLI for searching Libraries.io via the API
* [Picto](https://github.com/librariesio/picto) CLI for managing logos in Pictogram

### Other
* [Documentation](https://github.com/librariesio/documentation) Documentation for the whole Libraries.io project
* [Support](https://github.com/librariesio/support) Public issue tracker for Libraries.io users
* [Assets](https://github.com/librariesio/assets) Non-code assets for Libraries.io
* [GitHub Companion](https://github.com/librariesio/github_companion) Google chrome extension that adds Libraries.io to GitHub repo pages
* [D3 Dependencies](https://github.com/librariesio/d3-dependencies) D3 dependency graph visualization from Libraries.io API

### Retired repositories
* [Librarian](https://github.com/librariesio/librarian) Node.js web service for parsing dependencies from manifests
* [Librarian-parsers](https://github.com/librariesio/librarian-parsers) Node.js library for parsing dependencies from manifests
* [Librarian-cli](https://github.com/librariesio/librarian-cli) Node.js cli for parsing dependencies from manifests
* [Gem Parser](https://github.com/librariesio/gem_parser) Web service for parsing Ruby and Cocoapod manifests
* [GithubUrls](https://github.com/librariesio/github_urls) Parse GitHub repo details from a variety of urls
* [LibHub](https://github.com/librariesio/libhub) Minimalistic GitHub client for Node.js
* [Favicon](https://github.com/librariesio/favicon) Generates Libraries.io favicons for a given colour or language
* [First PR Bot](https://github.com/librariesio/firstprbot) Tweets whenever someone opens their first open source pull request on GitHub
* [Languages](https://github.com/librariesio/languages) Just the language names and colors from github-linguist

## TODO

Expand upon:

- GitHub Firehose
- Repository monitoring
- Repository Dependencies
- Distributed package managers (Carthage)
- Notifications
- Webhooks
- Deprecated and unmaintained detection
- Removal detection
- Recommendations
- Firehose
- Rest API
- Dependency warnings
- Project suggestions
- Project mutes
- Subscriptions
