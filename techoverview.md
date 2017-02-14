## Technical Overview
Libraries.io is made up of many smaller projects that work together to keep the [https://libraries.io](https://libraries.io) site running. The following diagram provides a high-level overview: 

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