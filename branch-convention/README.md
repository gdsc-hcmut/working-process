# Branch convention

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
