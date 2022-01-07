# Wiki
This is the Wiki of Hackathon Team `Brothers in Code`. It's includes some general informations.

## Team Sync
- Kanban Workflow
- Writing progress down daily (even if nothing happened)
	- What have I done today
	- Where will I continue working at
	- Do I have any Blockers - is someone able to help here
- Weekly meetings about Progress & Task Breakdown

### Git Guidelines
Follow the [Git Flow Workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)
1. Always work from feature branch with name convention `feature/{{TICKET-NUMBER}}` e.g. `feature/PIE-19` 
2. Link the feature Branch directly at your ticket by using the GitHub Power App (Choose your Ticket at Trello, click the GitHub Button, choose "Add Branch" and Link your Web-Reference)
3. Create a Merge Request if your Feature is Done and make a Notification in Slack with a direct link to your Merge Request
4. Merge into master only on approve
5. If you need to make a hot fix, use following schema: `hotfix/{{WHAT_NEED_TO_BE_FIXED}}`
6. Prefix your commit messages with the Ticket where you are working at (your Branch name) + a **meaningful** description. e.g. `PIE-19: setting up git wiki` 

### Ticket Sync with Trello
we are using Trello as a ticket manger (lol). There is currently just a single Board: [https://trello.com/b/M48OLhvy/gcp](https://trello.com/b/M48OLhvy/gcp)

#### Stages
- **Stories**: Do not move tickets from here to another stage. Stories describes our big goals and they include checkboxes with links to their subtickets
- **Backlog / ToDo**: These are all tickets where currently nobody is working at
- **W2C**: Wait to continue - if a ticket started, but not finished and you do not continue working at it, put it into this column
- **Is Blocked By**: If you already started working at a ticket and it's blocked by another ticket, put it into this Column
- **In Progress**: Tickets which are in Progress. Assign yourself to the ticket if you are currently working at it. Make sure that you have not more than 2 Tickets in Progress
- **R4R**: Ready for Review. If a ticket is done (includes all subtasks) this column is used. We will walk through that column together each friday
- **Done**: if a ticket is completely done.

### Links
- [Slack](https://join.slack.com/t/brothersincodegruppe/shared_invite/zt-10pfkhoh3-i7eqRaPHI1IZ8QQBkQxnCw)
- [Trello](https://trello.com/brothersincode2)
- [GitHub](https://github.com/JangasMonsterPlace)
- [Miro](https://miro.com/app/board/uXjVOZPHWTs=/?fromRedirect=1)

#### Ticket Rules
- Ticket should have a description
	- Put Link to Story in the first place of the description
	- If the ticket blocks other tickets, make a list with links to the tickets which are blocked by this ticket
	- If the ticket is blocked by other tickets, make a list with links to the tickets which are blocking this ticket
- Add a new ticket always into the checklist of the story where it's belongs to

## Past Hackathons & Projects
- Dec 7, 2021 - Feb 5, 2022 [Google Cloud Easy as Pie Serverless Hackathon by BeMyApp](https://www.eventbrite.de/e/google-cloud-easy-as-pie-serverless-hackathon-tickets-224293908117?keep_tld=1)
- Dec 10, 2021 - Dec 12, 2022 [Hack the Insight by NanoGiants](https://www.eventbrite.de/e/hack-the-insight-online-hackathon-for-ux-and-product-enthusiasts-tickets-203829187587)


### Hack the Insight by NanoGiants
We've build a review management framework with microservices by using Kafka and Python. 
See our last commits in following repositories - everything was build from scratch within 2 days:
- Webapp build with Flask in Backend, Bootstrap 4 in Frontend, Postgres Database and Elasticsearch. [Last commit](https://github.com/JangasMonsterPlace/flask-webapp/tree/bcc0efd58252e6beb2ef590bdcaab327efdcfa9c)
- ETL Framework with Python for Loading a Disney Review CSV file from GCP Cloud to Postgres and loading Tweets from Twitter to Postgres. [Last commit](https://github.com/JangasMonsterPlace/api-source-etl-scripts/tree/94786d264ad86924a371f3586f61dea6d10a9a3a)
- NLP with Python for finding Word Sequences and Topic Labeling with NLTK and Gensim. [Last commit](https://github.com/JangasMonsterPlace/nlp-processing/tree/cc6e641274d60a7e328584dd1b9ca4444c1fcde3)
- Event Trigger which pushes messages to Kafka for triggering executions in other microservices (kind of the "brain"). [Last commit](https://github.com/JangasMonsterPlace/job-runner/tree/9f5e1e4ecfae9d3a56346d194fb576c8056b06d0)
- Initial NLP planning with Jupyter Notebook. It was not in production and just for planning. [Last commit](https://github.com/JangasMonsterPlace/initial-nlp/tree/ed76fe7cc8ba61b2d778b11e580b72f3c27290fa)

### Team Members & Roles
- [snake-py](https://github.com/snake-py) - Developer
- [Talha-Altair](https://github.com/Talha-Altair) - DevOps
- [JangasCodingplace](https://github.com/JangasCodingplace) - Data Engineer

The result is used in different projects:
- a parallel Hackathon: [Google Cloud Easy as Pie Serverless Hackathon by BeMyApp](https://www.eventbrite.de/e/google-cloud-easy-as-pie-serverless-hackathon-tickets-224293908117?keep_tld=1)
- a private project for automatic finding relevant Influencers based on Blog texts
