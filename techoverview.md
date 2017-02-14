## Technical Overview

Libraries.io is made up of many smaller projects that work together to keep the [https://libraries.io](https://libraries.io) site running. The following diagram provides a high-level overview: 

![Overview of Libraries.io archiitecture](https://cloud.githubusercontent.com/assets/1060/22747144/19b1c3ea-ee1e-11e6-93ca-bf505ee5ee6f.png "Libraries.io Architecture")

Everything in Libraries.io begins with [package managers](https://github.com/librariesio/libraries.io/wiki/Package-Managers), on a regular basis background tasks find new or updated libraries from each of those packages managers, libraries cannot be added to the system unless they exist on one of those package managers.

Each library is stored in the [Project](https://github.com/librariesio/libraries.io/blob/master/app/models/project.rb) table, if that library's package manager supports published version numbers each new version is stored in the [Version](https://github.com/librariesio/libraries.io/blob/master/app/models/version.rb) table and if the package manager supports library dependencies then they are recorded in the [Dependency](https://github.com/librariesio/libraries.io/blob/master/app/models/dependency.rb) table.

Libraries.io will then augment package manager data with data from GitHub if one is referenced in the package manager. GitHub repositories will be downloaded and stored in the [GitHubRepository](https://github.com/librariesio/libraries.io/blob/master/app/models/github_repository.rb) table, on creation a background Sidekiq task is kicked off to download related information from GitHub including:

- [Readme](https://github.com/librariesio/libraries.io/blob/master/app/models/readme.rb)
- [Git tags](https://github.com/librariesio/libraries.io/blob/master/app/models/github_tag.rb)
- [Contributors](https://github.com/librariesio/libraries.io/blob/master/app/models/github_contribution.rb)
- Owner ([GitHub user](https://github.com/librariesio/libraries.io/blob/master/app/models/github_user.rb) or [GitHub Org](https://github.com/librariesio/libraries.io/blob/master/app/models/github_organisation.rb))
- Source repository (if it's a fork)
- [Dependency Manifests](https://github.com/librariesio/libraries.io/blob/master/app/models/manifest.rb)

Some package managers that don't have a concept of published versions (like Go and Bower), often they will fall back to using tags from a source repository if available, Libraries.io attempts to use GitHub tags as a fallback for all package managers that don't provide version information.

## Licenses

All license names are ran through the [SPDX](https://github.com/librariesio/spdx) gem to normalize as many different ways of writing the name of standard licenses into a single version, which is then used for filtering within search and listing on https://libraries.io/licenses Licenses are stored as arrays on projects, as a library can have multiple licenses. If a project has a non-standard or commercial license it's currently normalized to "Other" and is not indexed in search.

GitHub repositories have one license stored against them if provided by the [GitHub license API](https://developer.github.com/v3/licenses/), if a library doesn't have any license data from the package manager then it will fall back to using the GitHub license if it's source is on GitHub.

## Repositories

The main repositories are:

### Core
* [Libraries.io](https://github.com/librariesio/libraries.io) Main rails app

#### Manifest parsers
* [Librarian](https://github.com/librariesio/librarian) GitHub manifest parsing API service
* [Librarian Parsers](https://github.com/librariesio/librarian-parsers) Manifest parsers for Librarian
* [Librarian CLI](https://github.com/librariesio/librarian-cli) File based dependency manifest parsing
* [Bibliothecary](https://github.com/librariesio/bibliothecary)
* [Gem Parser](https://github.com/librariesio/gem_parser) Web service for parsing Ruby and Cocoapod manifests
* [Gemnasium Parser](https://github.com/librariesio/gemnasium-parser) An improved fork of gemnasium-parser
* [Carthage Parser](https://github.com/librariesio/carthage_parser) Web service for parsing Carthage manifests
* [mix-deps-json](https://github.com/librariesio/mix-deps-json) Elixir parser for Hex dependency manifests
* [clojars json](https://github.com/librariesio/clojars-json) Convert clojars.org data to JSON

### The API
[Firehose](https://github.com/librariesio/firehose) Server Sent Events API for Libraries.io releases

### Libraries
* [Languages](https://github.com/librariesio/languages) Just the language names and colors from github-lingust
* [Semantic Range](https://github.com/librariesio/semantic_range) node-semver written in Ruby for comparison and inclusion of semantic versions and ranges.
* [SemanticInterval](https://github.com/librariesio/semantic_interval) Turn Interval range syntax into SemVer range syntax
* [License Compatibility](https://github.com/librariesio/license-compatibility) Check compatibility between different SPDX licenses
* [SPDX](https://github.com/librariesio/spdx) A SPDX license normalizer
* [LibHub](https://github.com/librariesio/libhub) Minimalistic GitHub client for Node.js
* [GithubUrls](https://github.com/librariesio/github_urls) Parse GitHub repo details from a variety of urls
* [Pictogram](https://github.com/librariesio/pictogram) Logos for programming languages and package managers
* [Picto](https://github.com/librariesio/picto) CLI for managing logos in Pictogram
* [Favicon](https://github.com/librariesio/favicon) Generate Libraries.io favicons for a given colour or language
* [Package Managers](https://github.com/librariesio/package-managers) Metadata about every package manager that Libraries.io supports

### GitHub Firehose
* [Github Firehose](https://github.com/librariesio/github-firehose) Server Sent Events firehose of GitHub public timeline
* [GitHub Dispatch](https://github.com/librariesio/github-dispatch) Send events from the GitHub firehose into Sidekiq

### Webhooks
* [Lib2Issues](https://github.com/librariesio/lib2issues) Create GitHub Issues from Libraries.io webhooks
* [Travis Rebuilder](https://github.com/librariesio/travis-rebuilder) Rerun travis-ci tests after any dependency is updated
* [Sentinel](https://github.com/librariesio/sentinel) Automated dependency updates for Node.js projects

### Bots
* [Just Open Sourced](https://github.com/librariesio/justopensourced) Tweeting whenever a repo is open sourced on GitHub
* [First PR Bot](https://github.com/librariesio/firstprbot) Tweets whenever someone opens their first open source pull request on GitHub
* [Libby](https://github.com/librariesio/libby) Libraries.io hubot

### Other
* [Support](https://github.com/librariesio/support) Public issue tracker for Libraries.io users
* [Documentation](https://github.com/librariesio/documentation) Documentation for the whole Libraries.io project
* [Assets](https://github.com/librariesio/assets) Non-code assets for Libraries.io
* [GitHub Companion](https://github.com/librariesio/github_companion) Google chrome extension that adds Libraries.io to GitHub repo pages
* [D3 Dependencies](https://github.com/librariesio/d3-dependencies) D3 dependency graph visualization from Libraries.io API
* [Firehose Stream](https://github.com/librariesio/firehose-stream) Live streaming visualization of Libraries.io releases using the Firehose
* [libsearch](https://github.com/librariesio/libsearch) CLI for searching Libraries.io via the API
* [Required files (library)](https://github.com/librariesio/required_files) Ensure some files exist in all your repo's
* [Required files](https://github.com/librariesio/required-files) Files that should exist in every Libraries.io repository

## TODO

Expand upon:

- GitHub Firehose
- Repository monitoring
- Repository Dependencies
- Distributed package managers (Carthage)
- Notifications
- Webhooks
- SourceRank
- Deprecated and unmaintained detection
- Removal detection
- Recommendations
- Firehose
- Rest API
- Dependency warnings
- Project suggestions
- Project mutes
- Subscriptions