## Labelling 
Labelling is a key part of our workflow. We label issues by size, type or skills needed and drive parts of our process using them. Specificly we label tickets that are ideal for first time contributors or those that are part of our funded commitments. 

### Size
In the following *day* and *week* mean 'working approximately 7.5 hours per day, five days a week'. That is not to say any contributor is expected to work full-time on the project, but it should provide a truer sense of scale. 

* `micro` tickets require a trivial amount of work for someone with an existing, working environment and no longer than two hours for soemone starting afresh. It is likely that a micro ticket might also be perfect at a `first-pr` also (see below).
* `small` tickets require a an amount of work to replicate an issue and/or *should* take no longer than four hours for someone with a reasonable appreciation of the skills needed, the context and the project in general. 
* `medium` tickets require a reasonable amount of work to replicate an issue and/or *should* take no longer than a day or two for someone with a good understnading of the skills needed, the context and the project in general.
* `large` tickets require a considerable amount of work to replicate an issue and/or *will* take longer than a day or two for someone with an excellent understanding of the skills needed, the context and the project in general. It is advised that anyone embarking upon a large ticket discusses it with others through comments, in our public slack channel or at a weekly open call. See more about [contributing](/contributing.md).
* `epic` tickets require a considerable amount of work to replicate an issue and/or *will* take longer than a week for someone with expert understanding of the skills needed, the context and the project in general. Please do not embark upon an epic issue without first discussing it with members of the [core team](/coreteam.md), in our public slack channel or at a weekly open call. See more about [contributing](/contributing.md).

### Type or Skills
Projects typically indicate the type of issue, but we would like to be more explicit. We would like these labels to reflect the skills needed of the person who would ideally tackle it. This will lead to more effective prioritisation and enable contriutors who wish to learn these skills more scope to do so. Feel free to label a ticket with a number of skills needed. If a ticket requires more tha two skills consider splitting into two or more tickets. 

* `API` are issues regarding our own API. 
* `content` these isssues require a little word-smithing of new or existing copy. This might be grammar, phrasing, voicing or similar types of issue.
* `design` is for pure design. This might involde the creation of assets like logos, fonts, illustrations or it may be in support of frontend or UX issues. 
* `dependency parsing` in order to understand the relationships between libraries, their constituent components, and the projects they're included within, we have to parse dependency manifests. Sometimes these manifests require compilation, typically in the language or framework itself.
* `documentation` If an issue requires changes or clarification to our documentation (READMEs, wiki, code comments, etc.) then it will be marked with this label. These issues normally do not pertain to code changes and are ideal for those who don't necessarily want to get their hands dirty with code.
* `frontend` This relates to visual elements of the site that could be improved or are broken. This may be as simple as a change to a CSS colour or font size but may stretch all the way to things that do not render as expected on mobile devices. These are usually good issues for people with front-end development experience to tackle.
* `registry` Libraries.io gets it's data by scraping registries like package managers. Support for new registries or issues with current registries will be tagged with this label. 
* `research` in order to progress an issue or idea we may need more information about our own site, our users or more context regarding a problem for other sources. Any issue that needs a reasonable amount of information gathering will be tagged research. 
* `security` If you spot an issue related to security issues (e.g. invalid SSL certs, potential CSRF issues), mark it with this label. Always report zero-day issues through to zeroday@libraries.io to minimise impact to your fellow users!
* `sysops` is an issue about the automation and safe running of the environment on which the project runs. 
* `UX` These issues relate to how the site works, or more holistically, how the site *feels* to the end user, and will normally be related to the front-end of the website. These issues might typically relate to confusion stemming from navigation, form elements, input validation, or breaks in user flows.

### First-time Contributors
* `first-pr` will be used for any ticket ideal for a firs ttime contributor. These tickets will require minimal understnading of Libraries.io's strategy, architecture and minimal work to install a environment from which to work. 

### Funder Committments

* `funder-commitment` incidcates that the ticket is considered directly attributible to one of the [core team's](/coreteam.md) goals for which they receive financial support. You should discuss these issues with members of the core team before proceeding to work on it. 

### Process

* `On Hold` We will generally mark an issue as blocked if it requires more context for us to fix, is waiting on an updated version of a library that the issue depends on, or is waiting on a maintainer to do something before it can be answered. There may be other conditions in which we'll mark an issue as blocked, and we'll make this clear in the issue comments.
* `bug` An issue gets marked as a bug if (surprise!) the issue is linked to a bug in our code or something broken in our infrastructure. Bugs are usually the highest priority kind of issue as they will affect our users.
* `bugsnag` If an issue or exception in production code has been flagged via Bugsnag, it is labelled with this automatically.
* `duplicate` If an issue has been reported before, it will be marked with this label. This flags that a previous issue may not have been fixed as expected, or in the case of things we don't intend to fix or issues currently in discussion in another open issue, it means that we are likely to close the issue.
* `enhancement` These are improvements to the codebase that are "nice to have", and are usually medium to high impact but low importance. This includes improvements to features that already exist and may be assigned a milestone to give you an idea as to when it might be implemented. These are great for contributors that might have some extra spare time on their hands and would prefer to change existing code rather than add large chunks of brand new code.
* `feature` An issue will be marked with this label if it adds a new, discrete functional element to the codebase. They will generally require large amounts or effort to implement, require changes to both front-end view templates and back-end code, and assume prior knowledge of the codebase, making these the most tricky kinds of issues to close. However, they can be the most rewarding to close for the intrepid!
* `help wanted` Issues will be marked with this label by the maintainers if we'd like outside contributors to pitch in with code or opinions before we close them. These do not assume any skill level and are great opportunities for all members of our community to steer the direction of the project.
* `invalid` These are rare, and normally have been submitted in error.
* `needs rebase` You will find this label normally attached to pull requests, and means that the maintainers would like to you squash commits or rebase existing commits from master into your branch before we can merge your pull request. A maintainer will clarify this in the comment thread.
* `question` Issues can be marked with this label by anybody who would like other contributors or maintainers to answer a specific question before an issue can be closed. These normally do not assume any skill level (although may sometimes require maintainers to have the final say on them) and are great opportunities for all members of our community to steer the direction of the project.
* `refactoring` If an issue requires code to be refactored before a particular change can be made, or if you spot inelegant patterns or implementations in code that you feel could be better, then feel free to add this label to an issue. If the issue is the latter type, please be careful about the language you use in these threads. For example, things like "this code sucks!" or "you must be an idiot!" are unacceptable!. Programmers have feelings too and there are ways to suggest code changes without insulting people!
* `wontfix` This means that, after considering your issue in full, your issue is outside of [the intended scope of the project](/strategy.md) and is not something we'd like to add to the codebase right now or in the future. These are used sparingly and are intended to be rare, and are never used without reasoned justification.

### Optional
If you are a [committer](/committer.md) you may wish to consider adding the following labels, but they will not be enforced:

* `language` indicates the *predominant* coding language needed to tackle an issue. It is likely to be `Ruby`, `JavaScript` or `HTML`. Yes, srcipting and markup langauges are considered languages for this purpose.