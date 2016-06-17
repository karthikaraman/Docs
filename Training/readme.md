# Docs Training resources

This directory contains best practices, links, and resources for training those who wish to contribute to [docs.microsoft.com](docs.microsoft.com).

## Training 

### Beforehand

* A week or so in advance, set up a block of time (typically an hour or 90 minutes) to provide training for the contributors.

* At that time also send an introductory email to the contributors with a link to the [contributor's guide](https://github.com/Microsoft/Docs/tree/master/ContributorGuide), and ask that they preform the [tools and setup steps](https://github.com/Microsoft/Docs/blob/master/ContributorGuide/tools-and-setup.md) prior to the training. For those who entirely new to Git and Github, you may also suggest they take online training prior to the session:
   * The [Learn Git](https://www.codecademy.com/learn/learn-git) course from [Codecademy](https://www.codecademy.com).
   * The [Try Git](https://www.codeschool.com/courses/try-git) course from [Code School](https://www.codeschool.com]).
   * [GitHub's 15-minute interactive primer](https://try.github.io/), [cheat sheets](https://training.github.com/kit/), and [links to formalized training](https://services.github.com/).

### Training session

* Use the first third to explain Git and Github, using the [training PowerPoint Presentation](git-github-workflow-training.pptx).

* Use the second third to demonstrate our workflow using Gitbash, a markdown editor, and Github. While doing so, insist that the trainees follow along using their own installation of the tools. Have them:
   * Fork the repo
   * Clone their fork locally using `git clone http://github.com/GITHUBUSERNAME/REPO`
   * Create aliases to upstream and origin, and embed their credentials in the commandline using `git remote`
   * Sync their repo using `git pull upstream master`
   * Create a branch using `git branch BRANCHNAME` 
   * Change to their newly created branch using `git checkout BRANCHNAME`
   * Edit and/or add one or more files
   * Stage the files using `git add`
   * Commit the files using `git commit -m "COMMIT MESSAGE"`
   * Push the changes to Github using `git push origin BRANCHNAME`
   * Go to Github and create a pull request
   * View their changes in the staging site

* Leave the final third of the training session for questions (of which there will be many).

### Afterwards

* Follow up after the training to let the partners know that they can reply on you as a git/github/workflow SME.

* Actively seek out opportunities for the partners to make small changes and contributions to the documentation.

## Docs Repos

The current docs.microsoft.com repos are:

* Advanced Threat Analytics: [public](https://github.com/Microsoft/ATAdocs) | [private](https://github.com/Microsoft/ATAdocs-pr)
* Azure Rights Management: [public](https://github.com/Microsoft/Azure-RMSDocs) | [private](https://github.com/Microsoft/Azure-RMSDocs-pr)
* Docs (this repo): [public](https://github.com/Microsoft/Docs)
* Enterprise Mobility: [public](https://github.com/Microsoft/EMDocs) | [private](https://github.com/Microsoft/EMDocs-pr)
* Intune: [public](https://github.com/Microsoft/IntuneDocs) | [private](https://github.com/Microsoft/IntuneDocs-pr)
* Microsoft Identity Manager: [public](https://github.com/Microsoft/MIMDocs) | [private](https://github.com/Microsoft/MIMDocs-pr)
