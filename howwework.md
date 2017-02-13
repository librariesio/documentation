## Contributing to libraries.io
Thanks for considering conributing :heart:

These guidelines outline how to contribute to the [libraries.io](http://github.com/librariesio) project. 

## Table of Contents
TODO

## What's libraries.io About?
_Our goal is to raise the quality of all software_ 

By outlining our [mission and strategy](/stratey.md) we hope to give you more power to make decisions and determine how best to spend your time. Specifically we tackle three distinct problems:

* Discovery: _Helping developers make faster, more informed decisions about the software that they use._
* Maintainability: _Helping maintainers understand more about the software they depend upon, and producers to understand more about the consumers of their software._
* Sustainability: _Supporting undervalued software by highlighting shortfalls in contribution and funneling supportto them._

## What should I Know Before I Get Started?

### Code of Conduct
Libraries.io is an open and inclusive [community of people](/contributors.md) working together. We expect contributors to abide by our [contributor code of conduct](CODE_OF_CONDUCT.md) which basically say 'be excellent to each other'. Please report unacceptable behaviour to conduct@libraries.io

### Langauge
We communicate predominatly in English. That is contributions to the project should be made with English as the first language. We are happy for members of the community to communicate in a language other than English in chat, email and video but be aware that this might be considered exclusive by other members of the community. 

### Setup 
If you wish to make contributions to libraries.io then you'll need a local version of the site to test. You can find instructions to install the correct Ruby version, Postgres, and to set up the database in our [README](https://github.com/librariesio/libraries.io/blob/master/README.md#getting-started).

## How Can I Contribute? 

### Reporting Bugs

The simplest thing that you can do to help us is by filing good bug reports, so here we go:

#### Before Submitting a Bug Report

* Double-check that the bug is persistent, the site is still in it's infancy and sometimes artifacts may appear and disappear. 
* Double-check the bug hasn't already been reported [on our issue tracker](https://github.com/librariesio/libraries.io/issues?q=is%3Aissue+is%3Aopen+label%3Abug)

If something hasn't been raised, you can go ahead and create a new ticekt using the correct [template](/templates.md). If you'd like to help investigate further or fix the bug just mention it in your bug report and check out our [workflow](#workflow).

### Suggesting Enhancements

The next simplest thing you can do to help us is by telling us how we can improve the features we already support, here we go:

#### Before Submitting an Enhancement

* Check that the enhancement doesn't already exist by checking the site or our [changelog](https://github.com/librariesio/libraries.io/blob/master/changelog.md)
* Check that the enhancement is not already ticketed [on our issue tracker](https://github.com/librariesio/libraries.io/issues?q=is%3Aissue+is%3Aopen+label%3Aenhancement)

If the feature hasn't already been ticketed then go ahead and create a new ticket for it using the correct [template](/template.md). If you'd like to work on the enhancement then just mention it in a comment and check out our [workflow](#workflow).

### Suggesting New Features

If you're into this zone then you need to understnad a little more about what we're tryignt to achieve:

#### Before suggesting a feature

* Check that it aligns with [our strategy](strategy.md) and is specifically not in line with something we have said we will not do (for the moment this is anything to do with ranking *people*)
* Check that the feature is not already ticketed [on our issue tracker](https://github.com/librariesio/libraries.io/issues?q=is%3Aissue+is%3Aopen+label%3Afeature)
* Specifcally check that it is not already a [funded commitment](https://github.com/librariesio/supporters/issues).

If you're still thinking about that killer feature that no one else is thinking about then *please* ticket it up using the correct [template](/templates.md).

### Your First Contribution
You're in luck! We label issues that are ideal for first time contributors with `first-pr`. For someone who wants something a little more meaty you might find an issue that needs some assistance with the `help wanted` label. Next you'll want to read our [workflow](#workflow).

### Tackling Something Meatier

Tickets are labelled by size, skills required and to indicate workflow. Detailed can be found in our [labelling policy](/labelling.md). To get you started you might want to check out tickets concerning [documentation](https://github.com/librariesio/documentation/issues/), [user experience](https://github.com/librariesio/libraries.io/labels/UX)], [visual design](https://github.com/librariesio/libraries.io/issues/labels/visual%20design) or perhaps something already [awaiting help](https://github.com/librariesio/libraries.io/labels/help%20wanted). 

#### Before Diving in
You will find the following useful.

#### Overview
Libraries.io is many smaller projects that work together to keep the [libraries.io](https://libraries.io) service running. The main ones are:

Core
* [Libraries.io](https://github.com/librariesio/libraries.io) Main rails app

Manifest parsers
* [Librarian](https://github.com/librariesio/librarian) GitHub manifest parsing API service
* [Librarian Parsers](https://github.com/librariesio/librarian-parsers) Manifest parsers for Librarian
* [Librarian CLI](https://github.com/librariesio/librarian-cli) File based dependency manifest parsing
* [Bibliothecary](https://github.com/librariesio/bibliothecary)
* [Gem Parser](https://github.com/librariesio/gem_parser) Web service for parsing Ruby and Cocoapod manifests
* [Gemnasium Parser](https://github.com/librariesio/gemnasium-parser) An improved fork of gemnasium-parser
* [Carthage Parser](https://github.com/librariesio/carthage_parser) Web service for parsing Carthage manifests
* [mix-deps-json](https://github.com/librariesio/mix-deps-json) Elixir parser for Hex dependency manifests
* [clojars json](https://github.com/librariesio/clojars-json) Convert clojars.org data to JSON

The API
[Firehose](https://github.com/librariesio/firehose) Server Sent Events API for Libraries.io releases

Libraries
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

GitHub Firehose
* [Github Firehose](https://github.com/librariesio/github-firehose) Server Sent Events firehose of GitHub public timeline
* [GitHub Dispatch](https://github.com/librariesio/github-dispatch) Send events from the GitHub firehose into Sidekiq

Webhooks
* [Lib2Issues](https://github.com/librariesio/lib2issues) Create GitHub Issues from Libraries.io webhooks
* [Travis Rebuilder](https://github.com/librariesio/travis-rebuilder) Rerun travis-ci tests after any dependency is updated
* [Sentinel](https://github.com/librariesio/sentinel) Automated dependency updates for Node.js projects

Bots
* [Just Open Sourced](https://github.com/librariesio/justopensourced) Tweeting whenever a repo is open sourced on GitHub
* [First PR Bot](https://github.com/librariesio/firstprbot) Tweets whenever someone opens their first open source pull request on GitHub
* [Libby](https://github.com/librariesio/libby) Libraries.io hubot

Other
* [Support](https://github.com/librariesio/support) Public issue tracker for Libraries.io users
* [Documentation](https://github.com/librariesio/documentation) Documentation for the whole libraries.io project
* [Assets](https://github.com/librariesio/assets) Non-code assets for Libraries.io
* [GitHub Companion](https://github.com/librariesio/github_companion) Google chrome extension that adds Libraries.io to GitHub repo pages
* [D3 Dependencies](https://github.com/librariesio/d3-dependencies) D3 dependency graph visualization from Libraries.io API
* [Firehose Stream](https://github.com/librariesio/firehose-stream) Live streaming visualization of Libraries.io releases using the Firehose
* [libsearch](https://github.com/librariesio/libsearch) CLI for searching Libraries.io via the API
* [Required files (library)](https://github.com/librariesio/required_files) Ensure some files exist in all your repos
* [Required files](https://github.com/librariesio/required-files) Files that should exist in every Libraries.io repository

## How Can I Talk To Other Contributors?

### Chat
We use [Slack](http://slack.io) for chat. There's an open invitation avaialble to anyone who wishes to join the conversation at [http://slack.libraries.io](http://slack.libraries.io).

We try to use the following channels accordingly:

* `#general` channel is used for general, watercooler-type conversation, contributor updates and issue discusion.
* `#events` is used to share and discuss events that may be of interest to or attended by members of the community
* `#activity` contains notifications from the various platforms that we use to keep the libraries.io project turning. Including notfications from GitHub, Twitter and our servers. 

Members are encouraged to openly discuss their work, their lives, share views and ask for help using chat. It should be considered a *safe space* in which there is *no such thing as a stupid question*. Conversely no one contribtor should ever be expected to have read anything said in a chat. If someone should know soemthing then it should be written down as an issue and/or documented in an obvious place for others to find.  

### Video
[Google Hangouts](http://hangouts.google.com) is our preferred tools for video chat. We operate an [open hangout](http://bit.ly/2kWtYak) for anyone to jump into at any time to discuss issues face to face. 

### Regular updates
Contributors are encouraged to share what they're working on. We do this through daily or weekly updates in the `#general` channel on Slack. Updates should take the format 'currently working on X, expecting to move onto Y, blocked on Z' where x, y and z are issues in our [issue tracker](github.com/librariesio/issues). 

Additionally we host an [open hangout](http://bit.ly/2kWtYak) for any contributor to join at *5pm UTC on a Tuesday* to discuss their work, the next week's priorities and to ask questions of other contributors regarding any aspect of the project. Again this is considered a *safe space* in which *there is no such thing as a stupid question*.

### Mail
The [core team](https://github.com/orgs/librariesio/teams/core) operate a mailing list for project updates. If you'd like to subscribe you'll find a form in the footer on [libraries.io](http://libraries.io). 

### Twitter
We have an account on Twitter at [@librariesio](http://twitter.com/librariesio). This is predominatly used to retweet news, events and musings by controbutors rather than as a direct method of commmunication. Contributors are encouraged to use @librariesio in a tweet when talking about the project, so that we may retweet is appropriate. The account is moderated and protected by the [core team](https://github.com/orgs/librariesio/teams/core). 

### Facebook
We have a Facebook page at [@libraries.io](https://www.facebook.com/libraries.io). Again this is predominantly used to gather and reflect news, events and musings by contributors rather than as a direct method of communication. Contributors are encouraged to reference Libraries.io in a post when talking about the project, so that we may reflect this if appropriate. Again the account is moderated and protected by the [core team](https://github.com/orgs/librariesio/teams/core). 

### Medium
We have a Medium account at [@librariesio](https://medium.com/@librariesio) and once again it is used to reflect news, events and musings by contributors rather than a direct method of communication. Contributors are encouraged to reference @librariesio in a post when talking about the project, so that we may recommend it if appropriate. Again the account is moderated and protected by the [core team](https://github.com/orgs/librariesio/teams/core). 

## Workflow
In general we use [GitHub](https://help.github.com/) and [Git](https://git-scm.com/docs/gittutorial) to support our workflow. If you are unfamiliar with those tools then you should check them out until you feel you have a basic understanding of GitHub and a working understanding of Git. Specifcally you should understand how forking, branching, committing, PRing and merging works. 

#### Forking
We prefer that contributors fork the project in order to contribute.

#### Branching 
We *try* to use principles of [GitHub-flow](https://lucamezzalira.com/2014/03/10/git-flow-vs-github-flow/) in our branching model. That is the `master` branch will always be deployable to the live site, and that every branch from that will be used to add a feature, fix a bug, improve something or otherwise represent an atomic unit of work. 

#### Ticketing
We *try* to ticket everything. That is any bug, feature or enhancement that is worth an open, focussed and documented discussion. 

#### Labelling 
We agressively constrain labels as they are a key part of our workflow. Tickets will be labelled according to our [labelling policy](/labelling.md).

#### Templates
We use [templates](/templates.md) to guide contributors toward good practice in ticketing bugs, enhancements, features and in issueing pull-requests.

#### Commenting
If it posible to comment your contribution — for instance if you are contributing code — then do so in a way that is simple, clear, concise and lowers the level of understanding necessary for others to comprehend what comes afterward does or achieves. If you are contributing code it is very likely it will be rejected if it does not contain sufficient comments. 

#### Committing
When committing to a branch be sure to use plain, simple language that describes the incremental changes made on the branch toward the overal goal. Avoid unnecessary complexity or rationalisation. Simplify whenever possible. Assume a resonable but not comprehensive knowledge of the tools, techniques and context of your work. 

#### Submitting for Review
Once a peice of work (in a branch) is complete it should be readied for review. This might include [squashing commits](https://git-scm.com/book/en/v2/Git-Tools-Rewriting-History) in order to ease the load on others who will need to review the work that has been done. This is your last chance to ensure that your contribution is properly tested. If you are contributing code it is likely your contribution will be rejected if it would lower the test-coverage. Once this is done you can submit a pull-request following the [template](/templates.md).

It is likely that your contributions will need to be checked by at least one member of the [core team](https://github.com/orgs/librariesio/teams/core) prior to merging. It is also incredibly likely that your contribution may need some re-work in order to be accepted. Particualrly if it lacks an appropriate level of comments, tests or it is difficult to understand your commits. Please do not take offence if this is the case. We understnad that contributors give their time because they want to improve the project but please understand it is another's responsbility to ensure that the project is maintainable, and good practices like these are key to ensuring that is possible. 

#### Reviewing a PR
We appreciate that it may be difficult to offer constructive criticism, but it is a necessary part of ensuring the project is maintainable and successful. If it is difficult to understand something, request it is better commented. If you do not feel assured of the robustness of a contribution, request it is better tested. If it is unclear what the goal of the peice of work is and how it relates to the [strategy](/strategy.md), request a clarification in the corresponding ticket. If a pull-request has no corresponding ticket, decreases code coverage or otherwise decreases the quality of the project. Reject it. Otherwise, merge it. 

#### Merging
As we keep the `master` branch in a permenent state of 'deployment ready' once-merged your contribution will be live on the next deployment. 
#### Deploying 
Any member of the [deployers](https://github.com/orgs/librariesio/teams/deployers) team are able to redeploy the site. If you require a deployment then you might find one of them in our `#general` [chat channel on Slack](slack.libraries.io). 

