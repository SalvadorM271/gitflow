# Automate git flow

The main functionality of this repo is to create a chain reaction when we finish a feature and push it to the
main repository, which will then create a pull request for the review of the code, and when this pull request is approve
will be merge into the develop branch, same process will be repeated from develop to main.

This 3 main yml files execute the following functionality to make it possible:

workflow.yml ----------------- adds the version tag when there is a merge to main and deploys the page

pull_req_to_dev.yml ---------- when there is a push from the feature branch to main creates a pull request

pull_req_to_main.yml --------- when there is a push into develop creates a pull request to add code to main

Important

After pushing the changes to the feature branch, if all pull request were approve by the team and code was push to
our main branch is important to  remember to update our local develop and main branches with a git pull to avoid
conflicts.
