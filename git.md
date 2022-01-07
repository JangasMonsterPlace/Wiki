# Git Guidelines
Follow the [Git Flow Workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)
1. Always work from feature branch with name convention `feature/{{TICKET-NUMBER}}` e.g. `feature/PIE-19` 
2. Link the feature Branch directly at your ticket by using the GitHub Power App (Choose your Ticket at Trello, click the GitHub Button, choose "Add Branch" and Link your Web-Reference)
3. Create a Merge Request if your Feature is Done and make a Notification in Slack with a direct link to your Merge Request
4. Merge into master only on approve
5. If you need to make a hot fix, use following schema: `hotfix/{{WHAT_NEED_TO_BE_FIXED}}`
6. Prefix your commit messages with the Ticket where you are working at (your Branch name) + a **meaningful** description. e.g. `PIE-19: setting up git wiki`
