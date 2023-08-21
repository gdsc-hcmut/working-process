# Git Tag

## Create a git tag

Create a git tag:
```
git tag <tagname>
```
- For example: `git tag v1.0`

Create a git tag with annotation:
```
git tag -a <tag_name> -m <message>
```

These tag is just in local. We must push it to remote repo:
```
git push origin <tag_name>
```
Then, in main page of gitHub repo, we will see the **tag** that we have already push in **Releases**

<img src='https://github.com/gdsc-hcmut/working-process/assets/131350457/cf83a117-bc51-4c32-a8cc-8c7713142bdd' alt='releases' style="height:250px">