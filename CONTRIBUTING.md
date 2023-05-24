## Contribute to the project

This document contains information on how to contribute to the project. Please read it before you start contributing.

## Fork the repository

1. Go to the [repository page](https://github.com/ccdsiub/ml-essentials)
2. Click on code and then copy the HTTPS or SSH link (depending on your preference)
3. Open a terminal and navigate to the directory where you want to clone the repository
4. Type `git clone <link>` where `<link>` is the link you copied in step 2
5. Type `cd ml-essentials` to navigate to the cloned repository

## Create virtual environment

1. Type `python -m venv ml-venv` to create a virtual environment named `ml-venv`
2. Type `source ml-venv/bin/activate` for Linux or `ml-venv\Scripts\activate` for Windows to activate the virtual environment
3. Type `pip install -r requirements.txt` to install the required packages

## Create a new branch

1. Type `git checkout -b <branch-name>` where `<branch-name>` is the name of the branch you want to create
2. Type `git push -u origin <branch-name>` to push the branch to the remote repository

## Assign the branch to an issue

1. Go to the [issues page](https://github.com/ccdsiub/ml-essentials/issues) and select an issue or create a new one with the `New issue` button
2. If you are creating a new issue, fill in the title
3. Click on the `Assignees` button and select yourself if you are not already assigned to the issue
4. Click on the `Labels` button and select the appropriate label
5. Click on the `Projects` button and select the appropriate project
6. Click on the `Milestone` button and select the appropriate milestone
7. Click the gear icon next to `Development` and select the repository, then select the branch you created in the previous section and click `Apply`

## Make changes

1. Go to `docs/` and open the appropriate folder
2. Create a new file or edit an existing one
3. Go to `mkdocs.yml` and add the file to the `nav` section with the appropriate title and order
4. Run `mkdocs serve` to build the documentation and serve it locally
5. Go to `http://127.0.0.1:8000/` to view the site

## Commit changes and push to remote repository

1. Type `git add .` to add all the files you changed or `git add <file-name>` to add a specific file
2. Type `git commit -m "<commit-message>"` where `<commit-message>` is a short description of the changes you made, always start with a verb in the present tense (e.g. `Add documentation for the `ml-essentials` package`)
3. Fetch the latest changes from the `master` branch by typing `git pull origin master --rebase` and resolve any conflicts if necessary
4. Type `git push` to push the changes to the remote repository (always push to the branch you created in the previous section and not the `master` branch. Check the output of `git branch` to see which branch you are currently on)

## Create a pull request

1. Go to the [pull requests page](https://github.com/ccdsiub/ml-essentials/pulls)
2. Click on `New pull request`
3. Select the branch you created in the previous section as the `compare` branch
4. Select the `master` branch as the `base` branch
5. Click on `Create pull request` and fill in the title and description
6. If the pull request is related to an issue, type `Closes #<issue-number>` in the description where `<issue-number>` is the number of the issue
7. Assign the pull request to a reviewer
8. Add the appropriate labels, projects, and milestone
9. Click on `Create pull request`
10. Wait for the reviewer to review your changes and merge the pull request

## Remove the branch

1. If the pull request was merged and you want to remove the branch, go to the [pull requests page](https://github.com/ccdsiub/ml-essentials/pulls) view the closed pull requests and click on `Delete branch` at the bottom of the page to delete the branch
2. To clean up your local repository, type `git checkout master` to switch to the `master` branch and then type `git branch -d <branch-name>` where `<branch-name>` is the name of the branch you want to delete
3. Update your local `master` branch by typing `git pull origin master --rebase`

## For reviewers

1. Go to the [pull requests page](https://github.com/ccdsiub/ml-essentials/pulls) and select a pull request
2. Click on `Files changed` to view the changes
3. Check if the PR has changed/added any files in the `docs/` folder and if so, check if the files have been added to the `nav` section in `mkdocs.yml`
4. Check if the newly added codes follow good coding practice, for example, PEP8, avoiding redundancies. If not, point those out to be fixed.
5. If you notice some code that can be rewritten to improve efficiency by a significant amount, request to make that improvement.
6. Check the `Viewed` box at the bottom of the page to let the author know that you have reviewed the changes
7. Once you are done viewing the changes and satisfied with the changes, click on `Review changes` and select `Approve` to approve the changes. If you are not satisfied with the changes, write a comment and click on `Request changes` to request the author to make the changes.
8. Please do not merge the pull request. The maintainer will merge the pull request once all the reviewers have approved the changes.

That's it! You can now start working on a new issue. If you have any questions, please contact the project maintainer.
