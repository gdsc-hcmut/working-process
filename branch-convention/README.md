# Branch Convention

## Branch Name: 

- Feature branches: `feature/<id_of_issue>-<issue_name>`
- Bug branches: `bug/<id_of_issue>-<issue_name>`
- Chore branches: `chore/<id_of_issue>-<issue_name>`
- Document branches: `doc/<id_of_issue>-<issue_name>`
- If the change is small which is not required issue, then the branch name should be: `chore/<short_description>`

**Example**: Feature url filter with issue number 1211 will have branch name: `feature/1211-url-filter`

## Creating a new branch
- Must branch from **main**
- Must merge back into **main**
- Steps to create: 

`$ git checkout main`
  
`$ git fetch origin`

`$ git pull origin main`

`$ git checkout -b <branch_name>`

- Commit and push branch:

`$ git checkout main`

`$ git pull origin main`

`$ git checkout <branch_name>`

`$ git merge main`

`(resolve conflict)`

`$ git push origin <branch_name>`

## Merging branch

When a branch is merged back into main, we must use **Squash and merge** which only one commit from this branch will be added to base branch instead of all. This will help the commits in base branch more clearly and easy to track.

To setup **Squash and merge** as default, we go to setting. In **Pull Request**, we uncheck the other options.

<img src="https://github.com/gdsc-hcmut/working-process/assets/131350457/76c600c3-4aa9-48f2-9e04-59201ffc984f" alt="setup merging branch" style="height:250px">

