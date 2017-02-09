## How We Work
This document provides guidance on our working processes. How we communicate, how we ticket issues, how we contribute code, documentation, designs etc. and how we ensure that we are a growing group of happy, productive people. 

### Philosophy
Libraries.io is an open and inclusive [community of people](/contributors.md) working together. We expect contributors to abide by our [contributor terms](contributors.md) which basically say 'be excellent to each other'. 

We beleive strongly that if something is worth working on it should be written down, specifcally this should be in the form of an issue. If something is wrong, ticket it. If something is missing, ticket it. If something could be better... well, you might discuss it first, but then you'll probably ticket it. 

Similarly we think that how we work is as important as the work itself, which is why this document exists. The preceeding comment regarding ticketing applies to this document too. If something is unclear, ticket it. If something is unproductive, ticket it. If something is exclusive, ticket it. 

### Communication
We communicate predominatly in English. That is all contributions to the project should be made with English as the first language. We are happy for members of the community to communicate in a language other than English in chat, email and video but be aware that this might be considered exclusive and therefore against our philosophy if the working group is multi-lingual.

#### Chat
We use [Slack](http://slack.io) for chat. There's an open invitation avaialble to anyone who wishes to join the conversation at [http://slack.libraries.io](http://slack.libraries.io). Slack can be used in the browser or a [client for you operating system](https://slack.com/downloads).

We try to use the following channels accordingly:

* `#general` channel is used for general, watercooler-type conversation, contributor updates and issue discusion.
* `#events` is used to share and discuss events that may be of interest to or attended by members of the community
* `#activity` contains notifications from the various platforms that we use to keep the libraries.io project turning. Including notfications from GitHub, Twitter and our servers. 

Members are encouraged to openly discuss their work, their lives, share views and ask for help using chat. It should be considered a *safe space* in which there is *no such thing as a stupid question*. 

Conversely no one contribtor should ever be expected to have read anything said in a chat. As per our philosophy. If someone should know soemthing then it should be written down as an issue and/or documented in an obvious place for others to find.  

#### Video
[Google Hangouts](http://hangouts.google.com) is our preferred tools for video chat. We operate an [open chat room](http://bit.ly/2kWtYak) for anyone to jump into at any time to discuss issues face to face. 

#### Regular updates
Contributors are encouraged to share what they're working on. We do this through updates in the `#general` channel on Slack around 11am in your local timezone. Updates should take the format 'currently working on X, expecting to move onto Y, blocked on Z' where x, y and z are issues in our [issue tracker](github.com/librariesio/issues). 

Please be aware that contributors have different amount of time avaialble to contribute, work in different timezones and may have different working habit to other members. 

Additionally we host an open chat for any contributor to join at *5pm UTC on a Tuesday* to discuss their work, the next week's priorities and to ask questions of other contributors regarding any aspect of the project. Again this is considered a *safe space* in which *there is no such thing as a stupid question*.

#### Mail
The [core team](coreteam.md) operate a mailing list for project updates. If you'd like to subscribe you'll find a form in the footer on [libraries.io](http://libraries.io). 

We do not curently operate any mailing lists. If it becomes aparent that this would be a useful, additional mode of communication then Google's group-based mail subscription service would be our preference. 

#### Twitter
We have an account on Twitter at [@librariesio](http://twitter.com/librariesio). This is predominatly used to retweet news, events and musings by controbutors rather than as a direct method of commmunication. Contributors are encouraged to use @librariesio in a tweet when talking about the project, so that we may retweet is appropriate. The account is moderated and protected by the [core team](/coreteam.md). 

#### Facebook
We have a Facebook page at [@libraries.io](https://www.facebook.com/libraries.io). Again this is predominantly used to gather and reflect news, events and musings by contributors rather than as a direct method of communication. Contributors are encouraged to reference Libraries.io in a post when talking about the project, so that we may reflect this if appropriate. Again the account is moderated and protected by the [core team](/coreteam.md). 

#### Medium
We have a Medium account at [@librariesio](https://medium.com/@librariesio) and once again it is used to reflect news, events and musings by contributors rather than a direct method of communication. Contributors are encouraged to reference @librariesio in a post when talking about the project, so that we may recommend it if appropriate. Again the account is moderated and protected by the [core team](/coreteam.md). 

#### Marketing, PR and 'Corporate Voice'
Libraries.io is not a legal entity and it is not the product of any one individual. Nor should it be limited to the views and opinions of any one individual. Therefore libraries.io does not have its own voice and it does not do any direct marketing or PR. We rely on our community to think about, write and share their views in line with our open and inclusive philosophy. And we will do everything we can to gather and reflect this on the above channels for the other members of the community. 

### Workflow
Libraries.io is predominantly a software application. Most of the contributions to the project will be in the form of code. Therefore it follows that the general workflow should offer the best fit with the [developer workflow](/developerworkflow.md). If anything in the workflow seems overly taxing or irksome it is because it makes the process clearer for many other contributors.  

In general we use [GitHub](https://help.github.com/) and [Git](https://git-scm.com/docs/gittutorial) to support our workflow. If you are unfamiliar with those tools then you should check them out until you feel you have a basic understanding of GitHub and a working understanding of Git. Specifcally you should understand how forking, branching, committing, PRing and merging works. 

### Forking
We prefer that contributors fork the project in order to contribute to 'upstream'. This builds in redundancy (there will be many copies of libraries.io) and allows others to build upon the value our comminity has created, taking it in their own direction if desired. 

### Branching 
We *try* to use principles of [GitHub-flow](https://lucamezzalira.com/2014/03/10/git-flow-vs-github-flow/) in our branching model. That is the `master' branch will always be deployable to the live site, and that every branch from that will be used to add a feature, fix a bug, improve something or otherwise represent an atomic unit of work. 

#### Ticketing
We *try* to ticket everything that is worth a member of the community contributing to. That is any feature, bug, concept, view or revelation that is worth an open, focussed and documented discussion. This includes things like 'should we add a feature that produces a leaderboard of people in open source?' (the answer is no) but not 'where can I find the documentation for ticketing?'. Questions are for our chatroom, a video call or as a last resort the [support repo](http://github.com/librariesio/support). We use [templates](http://github.com/librariesio/awesome-github-templates) to guide contributors toward good practice.

#### Labelling 
We agressively constrain labels as they are a key part of our workflow. Tickets should be labelled according to out [labelling policy](/labelling.md). Any ticket that does not satisfy the policy will be edited to do so or rejected outright. 

#### Templates
We use [templates](http://github.com/librariesio/awesome-github-templates) to guide contributors toward good practice in ticketing issues, bugs, features etc. and in issueing pull-requests. We strongly advise but do not enforce the use of templates as we understand that some contributors may find it difficult to frame their ticket or pull-request within the confines of a template. 

#### Commenting
If it posible to comment your contribution — for instance if you are contributing code — then do so in a way that is simple, clear, concise and lowers the level of understanding necessary for others to comprehend what comes afterward does or achieves. If you are contributing code it is very likely it will be rejected if it does not contain sufficient comments. 

#### Committing
When committing to a branch be sure to use plain, simple language that describes the incremental changes made on the branch toward the overal goal. Avoid unnecessary complexity or rationalisation. Simplify whenever possible. Assume a resonable but not comprehensive knowledge of the tools, techniques and context of your work. 

#### Submitting for Review
Once a branch (regarding an atomic unit of work) is complete it should be readied for review. This might include [squashing commits](https://git-scm.com/book/en/v2/Git-Tools-Rewriting-History) in order to ease the load on others who will need to review the work that has been done. This is your last chance to ensure that your contribution is properly tested. If you are contributing code it is likely your contribution will be rejected if it would lower the test-coverage. Once this is done you can submit a pull-request. It will then be reviewed by other members of the community. 

#### Reviewing
It is likely that your contributions will need to be checked by at least one member of the [core team](/coreteam.md) or [deployers](/deployers.md) prior to merging. It is also incredibly likely that your contribution may need some re-work in order to be accepted. Particualrly if it lacks an appropriate level of comments, tests or it is difficult to understand your commits. Please do not take offence if thsi is the case. We understnad that contributors give their time because they want to improve libraries.io. Similarly it is other contributor's responsbility to ensure that the project is maintainable and good practices like these are key to ensuring that is possible. 

For reviewers: we appreciate that it may be difficult to offer constructive criticism, but it is a necessary part of ensuring the project is maintainable and successful. If it is difficult to understand something, request it is better commented. If you do not feel assured of the robustness of a contribution, request it is better tested. If it is unclear what the goal of the peice of work is and how it relates to the [strategy](/strategy.md), request a clarification in the corresponding ticket. If a pull-request has no corresponding ticket, decreases code coverage or otherwise decreases the quality of the project. Reject it. Otherwise, merge it. 

#### Merging
As we keep the `master' branch in a permenent state of 'deployment ready' once-merged your contribution will be live on the next deployment. 
#### Deploying 
Any member of the [deployers](/deployers.md) team are able to redeploy the site. If you require a deployment then you might find one of them in our `#general' [chat channel on Slack](slack.libraries.io). 

