# Setup Codeowners

## Add Codeowners

Create a file name **CODEOWNERS** and put in **.github/** directory in the root of your repo.

Then, go to **Settings**, choose branch and select to protect **main** branch. In **Protect matching branches**, checking these following boxes:

- **Require a pull request before merging**
- **Require approvals**, then choose the approvals number
- **Require review from Code Owners**
- **Do not allow bypassing the above settings**

With these rules, each pull request must be reviewed by the person that we have defined in **CODEOWNERS** before it can be merged.

## Syntax Of CODEOWNERS:
These owners will be the default owners for everything in
the repo. Unless a later match takes precedence,
@global-owner1 and @global-owner2 will be requested for
review when someone opens a pull request.

`*   @global-owner1 @global-owner2`

Order is important; the last matching pattern takes the most
precedence. When someone opens a pull request that only
modifies JS files, only @js-owner and not the global
owner(s) will be requested for a review.

`*.js    @js-owner`

You can also use email addresses if you prefer. They'll be
used to look up users just like we do for commit author
emails.

`*.go    docs@example.com`

In this example, @doctocat owns any files in the build/logs
directory at the root of the repository and any of its
subdirectories.

`/build/logs/   @doctocat`

The **docs/*** pattern will match files like
**docs/getting-started.md** but not further nested files like
**docs/build-app/troubleshooting.md**.

`docs/*  docs@example.com`
