## Labelling 
Labelling is a key part of our workflow. We label issues by size, type or skills needed and drive parts of our process using them. Specificly we label tickets that are ideal for first time contributors or those that are part of our funded commitments. 

We will enforce this policy to ensure that new contributors and existing contributors alike are as productive and efficient with their time as possible. This may include modifying labels or rejecting a ticket if is does not comply with the following:

### Size
In the following *day* and *week* mean 'working approximately 7.5 hours per day, five days a week'. That is not to say any contributor outside of the [core team](/coreteam.md) is expected to work full-time on the project, but it should provide a truer sense of scale. 

* `micro` tickets require a trivial amount of work for someone with an existing, working environment and no longer than two hours for soemone starting afresh. It is likely that a micro ticket might also be perfect at a `first-pr` also (see below).
* `small` tickets require a an amount of work to replicate an issue and/or *should* take no longer than four hours for someone with a reasonable appreciation of the skills needed, the context and the project in general. 
* `medium` tickets require a reasonable amount of work to replicate an issue and/or *should* take no longer than a day or two for someone with a good understnading of the skills needed, the context and the project in general.
* `large` tickets require a considerable amount of work to replicate an issue and/or *will* take longer than a day or two for someone with an excellent understanding of the skills needed, the context and the project in general. It is advised that anyone embarking upon a large ticket discusses it with others through comments, in our public slack channel or at a weekly open call. See more about [how we work](/howewework.md).
* `epic` tickets require a considerable amount of work to replicate an issue and/or *will* take longer than a week for someone with expert understanding of the skills needed, the context and the project in general. Please do not embark upon an epic issue without first discussing it with members of the [core team](/coreteam.md), in our public slack channel or at a weekly open call. See more about [how we work](/howewework.md).

### Type or Skills
Projects typically indicate the type of issue, but we would like to be more explicit. We would like these labels to reflect the skills needed of the person who would ideally tackle it. This will lead to more effective prioritisation and enable contriutors who wish to learn these skills more scope to do so. Feel free to label a ticket with a number of skills needed. If a ticket requires more tha two skills consider splitting into two or more tickets. 

* `API` 
* `content`
* `design`
* `documentation`
* `illustration`
* `licensing`
* `package manager`
* `rank`
* `security`
* `sysops`
* `testing`
* `UX`
* `research`

### First-time Contributors
* `first-pr` will be used for any ticket ideal for a firs ttime contributor. These tickets will require minimal understnading of libraries.io's strategy, architecture and minimal work to install a environment from which to work. 

### Funder Committments

* `funder-commitment` incidcates that the ticket is considered directly attributible to one of the [core team's](/coreteam.md) goals for which they receive financial support. You should discuss these issues with members of the core team before proceeding to work on it. 

### Process

* `bug` idocuments a bug, there's a [template](templates.md) for bug reporting that we expect contributors to follow.
* `blocking` iis currently blocked by another ticket, specifically one that is currently in progress.
* `duplicate` is a duplicate of another ticket. Consesnus should be reached on which ticket should remain open.
* `enhancement` describes a 'nice to have' rather than 'essential' feature. It may have fallen out of an essential feature. There's a [template](/templates.md) for feature requests. 
* `feature` describes an atom unit of work that has enough granularity for an individual contributor to work on it, there's a [template](/templates.md) for feature requests.
* `help wanted` may currently be blocked (see blocking) or require some input from someone else in the community.
* `hold` is used to indicate a ticket that explicitly should not be picked up by a contributor at this time, most likely because it is dependent on other features, is in the [roadmap](/roadmap.md) or is one of the [core team's](/coreteam.md) [funded commitments](http://gituhub.com/librariesio/supporters).
* `in progress` is a ticket currently allocated to a contributor and is actively being worked on.
* `needs rebase` is a ticket that needs some attention to simplify the structure of contributions. 
* `question` is a ticket that requires input from the community of users and/or contributors
* `refactoring` is a ticket that will require an understanding of the project as it involved re-structuring, it's unlikely and refactoring ticket will be micro or small. 
* `wontfix` is a ticket that will explicitly not be fixed because it is against our [strategy](strategy.md) or [roadmap](roadmap.md).

### Optional
If you are a [committer](/committer.md) you may wish to consider adding the following labels, but they will not be enforced:

* `language` indicates the *predominant* coding language needed to tackle an issue. It is likely to be `Ruby`, `JavaScript` or `HTML`. Yes, srcipting and markup langauges are considered languages for this purpose.