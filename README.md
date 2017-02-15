## Welcome to Libraries.io :tada:
Here you'll find guidance for contributors and documentation for the Libraries.io project as a whole.

### Assumptions
We have made the following assumptions in our guidance and documentation:

* that the reader has a basic understanding of the collaborative coding platform [GitHub](https://help.github.com/),
* that the reader has a working understanding of the distributed revision control system [Git](https://git-scm.com/docs/gittutorial),
* that the reader is able to communicate, in writing, in English. 

## Why Build Libraries.io?
_Our goal is to raise the quality of all software._

We do this by tackling three problems:

* Discovery: _Helping developers make faster, more informed decisions about the software that they use._
* Maintainability: _Helping maintainers understand more about the software they depend upon and the consumers of their software._
* Sustainability: _Supporting undervalued software by highlighting shortfalls in contribution and funneling support to them._

If you'd like to know why we think this is the right approach then check out [our strategy](/strategy.md). 

## How Does Libraries.io Work?
Libraries.io collects data about software and the frameworks, plugins and tools they depend upon which we collectively call libraries.

Everything in Libraries.io begins with [package managers](/packagemanagers.md), on a regular basis background tasks find new or updated libraries from each of those packages managers. Each library is stored as a project alongside any data we can gleam from the package manager. If the package manager provides a link to a hosted revision control service like GitHub then Libraries.io fetches yet more data from there. 

Using the data collected we then calculate the [SourceRank](/sourcerank.md), this value is used to index the project in search results. Next we highlight any issues regarding updates, deprecated versions, yanked or deleted libraries, license incompatibilities etc. to maintainers who depend on a given library. Finally we highlight undervalued and under-supported libraries, guiding maintainers toward projects that they could contribute to that would have a direct benefit on their own work. 

If you'd like an in-depth technical overview, including a description of each of the repositories in the Libraries.io organisation and how they work together then check out our [technical overview](/techoverview.md).

## How Can I Help?
If you wish to contribute to Libraries.io must agree to our [contributor terms](/CONTRIBUTORS.md). In short they say: be excellent to one another. If you're able to abide by those terms then check out our [contributor's handbook](CONTRIBUTING.md).

## Improving This Document
You can view the source for this document and the rest of our documentation [on GitHub](https://github.com/librariesio/documentation). You can also view, comment upon and create new issues concerning this documentation [on our issue tracker](https://github.com/librariesio/documentation). For more information about contributing to Libraries.io please read our [contributor's handbook](/contributorhandbook.md).